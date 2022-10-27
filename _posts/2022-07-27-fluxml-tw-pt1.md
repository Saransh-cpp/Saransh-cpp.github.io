---
layout: post
title:  My experience working as a Technical Writer with FluxML
date:   2022-07-27
description: One thing that open-source can’t get enough of is documentation!
tags: fluxml julia machine-learning technical-writing
categories: experience
---

<p align="center">
    <img src="https://miro.medium.com/max/1400/0*lKBsvZlO7OvUuBhM" width="70%"/>
</p>

> “One thing that open-source can’t get enough of is documentation”
> 
> — Anonymous

(Same post, but on [medium](https://blog.devgenius.io/my-experience-working-as-a-technical-writer-with-fluxml-2c19ab814089) (I am migrating my blogs from medium to my website))

This summer, I started working as a technical writer with `FluxML` under `Julia Season of Contributions`, and as expected, this experience was very different from writing code.

During the beginning of the summer, I decided to take up a technical writer’s job that involved writing documentation and tutorials for Machine Learning. At the same time, I was learning `Julia`, and the `FluxML` ecosystem sounded like a perfect place for me. I applied for the position through Google Season of Docs but unfortunately couldn’t get in because of limited openings. Fortunately, the `Julia` Language decided to fund me for the next few months to work on `FluxML` under Julia Season of Contributions!

In the following blog, I will share my experience and the work I have done so far as a part of Julia Season of Contributions!

<p align="center">
    <img src="https://miro.medium.com/max/1034/0*q6JXOCVKV1iFaSdF.jpg" width="60%"/>
</p>

## Doctests

<p align="center">
    <img src="https://miro.medium.com/max/1400/0*8GSRfjMTA_bTMlYF.jpg" width="60%"/>
</p>

`Flux`’s documentation lacked doctests, making its code examples stale after each release. Further, many current examples thought to be covered by doctests, were already outdated.

Some of the doctests were straightforward to add, but most of them require in-depth discussions with the mentors and the community members. In addition, the documentation written in markdown format also required periodic testing to ensure that the changing API does not break the examples.

`Flux` now has doctests written for every single public API, and most of the markdown example are also covered under these doctests. Some of these changes haven’t been merged yet, but they are under review!

## Missing docstrings

<p align="center">
    <img src="https://miro.medium.com/max/1006/0*8kn0CXy4r7I1OXw6.jpg" width="50%"/>
</p>

Some of `Flux`’s public API is also undocumented, or has a relatively less clear documentation. For example, most of the neural network layers provided by `Flux` have two constructors — one for initializing layers with pre-defined weights and biases and another for generating weights and biases from a distribution. In most cases, only one constructor was documented, and the other was not.

Other such instance of missing docstrings was `Flux`‘s manual. Here the docstrings were present in the codebase, but they were not present in the manual. Such cases were solved by adding the docstrings to the manual or creating a new section for such missing docstrings.

In addition to `Flux`, other packages under FluxML also had a similar problem. Some of these packages like `NNLib.jl`, `Zygote.jl`, `Optimisers.jl`, `Functors.jl`, and `MLUtils.jl` (under `JuliaML`) were also referenced in `Flux`‘s documentation. The missing docstrings in these packages were transmitted to `Flux`‘s docs, resulting in even more missing docstrings.
All the missing docstrings have now been added to the respective manuals and functions, including that of other `FluxML` packages!

## Broken documentation

<p align="center">
    <img src="https://miro.medium.com/max/1000/0*MarZNCzdnOb8c2vy.jpg" width="50%"/>
</p>

Documentation is incomplete without cross-references, and `Julia`’s wonderful documentation package makes this easy. `Flux` has these cross-references in place, but some of them lead to nowhere.

Additionally, some of the docstrings were not rendered correctly in the manual. These instances of broken documentation have been fixed, and once the PR is merged, users should not see 404 pages or un-rendered docstrings anymore!

## CI/CD

<p align="center">
    <img src="https://miro.medium.com/max/1400/0*k6C11T4CR0B75GMy.jpg" width="50%"/>
</p>

The user-facing documentation is facilitated by a CI/CD service, which keeps this documentation deployed and available to users at all times. It is also common for open-source projects to open-source their deployment recipes.

`FluxML`‘s ecosystem had some minor issues in this CI service. Zygote.jl had doctests running twice, using twice the CI time and resources, and on the other hand, `Flux` specified different versions of Julia in its CI and `make.jl` file.

Further, `Documenter.jl` allows a user to generate documentation previews for pull requests, and `Flux` had a bot set up to facilitate this, but it was down for a long time. In addition, these documentation previews are collected in the `gh-pages`` branch, which was getting very bulky and had to be cleaned up with an automated workflow. I restarted this bot and added a workflow for cleaning these generated previews periodically!

Finally, I also fixed some issues in `Optimisers.jl`‘s documentation that were causing its CI to fail.

## FluxML’s ecosystem

The `FluxML` ecosystem, in addition to `Flux.jl`, also had some documentation problems. For instance, `Optimisers.jl` and `Zygote.jl` had shortcomings in their CI suite, which have been discussed above. Similarly, `Functors.jl` and `MLUtils.jl` had broken documentation, missing docstrings, and an incomplete manual, which has also been discussed in great detail above!

Lastly, the “ecosystem” pages present on `Flux`‘s website and documentation were out of sync and had redundant information. The “ecosystem” page was completely revamped and updated with the latest advancements related to Machine Learning in `Julia`!

## Minor code changes

Yes! The documentation changes were also accompanied by minor code changes!

`Flux`‘s public and internal API is very hard to differentiate if you are new to the codebase; hence, newcomers used to find it hard to navigate through this. The API was made clear by removing internal instances from the documentation and prepending an underscore to the internal API.

Furthermore, I also stumbled upon a bug while writing doctests for tversky loss. The tversky loss has two parameters, `α`, and `β`, and `Flux` internally calculates the value of `α` as `1-β`. The loss mathematically is defined as `1-tversky index`, and the `tversky index` mathematically is defined as:

> S(P, G; α, β) = |P G| / (|P G| + α|P \ G| + β|G \ P|)
>
> where α and β control the magnitude of penalties for FPs and FNs, respectively.

Flux implements the loss in the following way -

{% highlight julia %}1 — sum(|y .* ŷ| + 1) / (sum(y .* ŷ + β*(1 .- y) .* ŷ + (1 — β)*y .* (1 .- ŷ)) + 1){% endhighlight %}

with the following code -

{% highlight julia linenos %} """
     tversky_loss(ŷ, y; β = 0.7)

 Return the [Tversky loss](https://arxiv.org/abs/1706.05721).
 Used with imbalanced data to give more weight to false negatives.
 Larger β weigh recall more than precision (by placing more emphasis on false negatives)
 Calculated as:
     1 - sum(|y .* ŷ| + 1) / (sum(y .* ŷ + β*(1 .- y) .* ŷ + (1 - β)*y .* (1 .- ŷ)) + 1)
 """
 function tversky_loss(ŷ, y; β = ofeltype(ŷ, 0.7))
     _check_sizes(ŷ, y)
     #TODO add agg
     num = sum(y .* ŷ) + 1
     den = sum(y .* ŷ + β * (1 .- y) .* ŷ + (1 - β) * y .* (1 .- ŷ)) + 1
     1 - num / den
 end
{% endhighlight %}

Notice how the term `(1 .- y) .* ŷ` (False Positives) is multiplied by `β`, whereas it should be multiplied with `α` (which is `1-β`). Similarly, the term `y .* (1 .- ŷ)` is multiplied with `α` (that is `1-β`), whereas it should be multiplied with `β`.

This detail makes the loss function behave in a manner opposite to its documentation. For example -

{% highlight julia %}julia> y = [0, 1, 0, 1, 1, 1];

julia> ŷ_fp = [1, 1, 1, 1, 1, 1]; # 2 false positive -> 2 wrong predictions

julia> ŷ_fnp = [1, 1, 0, 1, 1, 0]; # 1 false negative, 1 false positive -> 2 wrong predictions

julia> Flux.tversky_loss(ŷ_fnp, y)
0.19999999999999996

julia> Flux.tversky_loss(ŷ_fp, y) # should be smaller than tversky_loss(ŷ_fnp, y), as FN is given more weight
0.21875
{% endhighlight %}

Here the loss for `ŷ_fnp`, `y` should have been larger than the loss for `ŷ_fp`, `y` as the loss should give more weight or penalize the False Negatives (default `β` is `0.7`; hence it should give more weight to FN), but the exact opposite happens.

Changing the implementation of the loss yields the following results -

{% highlight julia %}julia> y = [0, 1, 0, 1, 1, 1];

julia> ŷ_fp = [1, 1, 1, 1, 1, 1]; # 2 false positive -> 2 wrong predictions

julia> ŷ_fnp = [1, 1, 0, 1, 1, 0]; # 1 false negative, 1 false positive -> 2 wrong predictions

julia> Flux.tversky_loss(ŷ_fnp, y)
0.19999999999999996

julia> Flux.tversky_loss(ŷ_fp, y) # should be smaller than tversky_loss(ŷ_fnp, y), as FN is given more weight
0.1071428571428571
{% endhighlight %}

which looks right!

(This bug has not been confirmed by someone other than me yet, and the fix is still under review.)

## Getting started section

`Flux` has a lot of tutorials and examples, but they are scattered around and very hard to navigate through. The current “Getting Started” section, “Overview” section, and “Basics” section have valuable information for beginners, but the information is scattered among these three sections.

Additionally, one of these three sections is on Flux’s website, and two are available on the documentation website, making it difficult for newcomers to navigate between these hackable yet basic examples. Instead, these three tutorials could be moved out of their current places and combined under a single section named “Getting Started”, which could then be added to the documentation and linked on the website.

I have started working on this section, and two extensive tutorials have already been added as PRs: one on linear regression (with and without `Flux`) and one on logistic regression (with and without `Flux`). These PRs are currently under review and should be merged in the upcoming weeks.

---

I have had an incredible time contributing to `Flux` and its neighbor repositories, and I hope to continue these contributions with the same momentum. I have also learned a lot, including that documentation additions require more discussions than code additions.

This work wouldn’t have been possible without my mentor `@DhairyaLGandhi` and a lot of other `FluxML`’s maintainers (`@ToucheSir`, `@mcabbott`, `@CarloLucibello`, `@darsnack`). They have been very patient with my questions and messy PRs 😆

---

## Tweets

Follow me on Twitter :)

{% twitter https://twitter.com/saranshchopra7/status/1532365616610672640 %}

---

## Appendix

### Pull requests
##### Flux.jl
- [Add a ton of doctests + fix outdated documentation in .md files](https://github.com/FluxML/Flux.jl/pull/1916)
- [Update docstrings of basic.jl and conv.jl](https://github.com/FluxML/Flux.jl/pull/1978)
- [Update docstrings in upsample.jl, recurrent.jl, and normalise.jl](https://github.com/FluxML/Flux.jl/pull/1995)
- [Miscellaneous docstring additions and fixes](https://github.com/FluxML/Flux.jl/pull/1998)
- [Add MLUtils’s docs and fix some missing docstrings](https://github.com/FluxML/Flux.jl/pull/1910)
- [Turn off doctests while building docs](https://github.com/FluxML/Flux.jl/pull/1915)
- [Unify ecosystem.md](https://github.com/FluxML/Flux.jl/pull/1923)
- [Get the DocBot up again!](https://github.com/FluxML/Flux.jl/pull/1937)
- [Add a workflow to delete PR previews](https://github.com/FluxML/Flux.jl/pull/1943)
- [Get rid of documentation warnings and 404 pages](https://github.com/FluxML/Flux.jl/pull/1987)
- [Create a getting started section and add a new linear regression example](https://github.com/FluxML/Flux.jl/pull/2016)
- [Add a logistic regression example to the Getting Started section](https://github.com/FluxML/Flux.jl/pull/2021)

#### Zygote.jl
- [Run doctests only once](https://github.com/FluxML/Zygote.jl/pull/1255)

#### Optimisers.jl
- [Fix the doctests and the broken CI](https://github.com/FluxML/Optimisers.jl/pull/98)

#### Functors.jl
- [Fix missing docs and cross-references](https://github.com/FluxML/Functors.jl/pull/42)

#### MLUtils.jl
- [Add missing docstrings to the manual](https://github.com/JuliaML/MLUtils.jl/pull/95)

### Issues / discussions
#### Flux.jl
- [Missing docstring for Flux.Data.Dataloader](https://github.com/FluxML/Flux.jl/issues/1909)
- [Different Julia versions at different places for doctests](https://github.com/FluxML/Flux.jl/issues/1914)
- [Inconsistent “Julia ecosystem” docs](https://github.com/FluxML/Flux.jl/issues/1922)
- [Add a workflow to clean-up gh-pages branch?](https://github.com/FluxML/Flux.jl/issues/1940)
- [Discussion: doctests, docstrings, documentation manual, and unclear internal API (for newcomers)](https://github.com/FluxML/Flux.jl/issues/1990)
- [Bug: Swapped alpha and beta in tversky loss?](https://github.com/FluxML/Flux.jl/issues/1993)
- [Discussion: Revamped Getting Started guide](https://github.com/FluxML/Flux.jl/issues/2012)

#### Zygote.jl
- [Doctests running twice](https://github.com/FluxML/Zygote.jl/issues/1199)

---

## Bonus

<p align="center">
    <img src="https://miro.medium.com/max/1344/0*2SLqKWtR_dGZwRAm.jpg" width="60%"/>
</p>
