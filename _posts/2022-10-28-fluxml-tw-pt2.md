---
layout: post
title:  My experience working as a Technical Writer with FluxML - Part 2
date:   2022-10-28
description: One thing that open-source can’t get enough of is documentation!
tags: fluxml julia machine-learning technical-writing open-source
categories: experience
---

<p align="center">
    <img src="https://miro.medium.com/max/1400/0*lKBsvZlO7OvUuBhM" width="70%"/>
</p>

> “One thing that open-source can’t get enough of is documentation”
>
> — Anonymous

I have finally completed my official period as a Technical Writer at `FluxML`, and I have enjoyed every second of it! This blog serves as a summary of the work done during the second half of my time at `FluxML`. You'd notice that the contributions listed in this blog would cover the entire `FluxML` ecosystem and not just `Flux.jl`. Furthermore, I will also list some additional documentation contributions made to the much larger `Julia` ecosystem during this period!

A quick introduction to `FluxML`, quoting their documentation -

> Flux is a 100% pure-Julia stack and provides lightweight abstractions on top of Julia's native GPU and AD support. It makes the easy things easy while remaining fully hackable.
>
> Flux is a library for machine learning geared towards high-performance production pipelines. It comes "batteries-included" with many useful tools built in, but also lets you use the full power of the Julia language where you need it.

Honestly, the nature of my work at `FluxML` diverged so quickly that summarising it would be a difficult task, but I will try my best! Buckle up! Psst, you can find more about the first half of the time spent at `FluxML` [here](http://saransh-cpp.github.io/blog/2022/fluxml-tw-pt1/).

## Getting started section

Let's start from where I left the last blog - the new "Getting Started" section. The good news is that `Flux` has a better structured "Getting Started" section now! The bad news is that I did not work on it, but the second good news is that it turned out better than the one I had in mind!

`Flux` had a lot of tutorials and examples, but they were scattered around and very hard to navigate through. The old “Getting Started” section, “Overview” section, and “Basics” section had valuable information for beginners, but the information was scattered among these three sections. Now, all of these sections have been combined (a huge thanks to [`@mcabbott`](https://github.com/mcabbott)) in a single "Getting Started" section in `Flux`'s docs! We still have a Getting Started page on `Flux`'s website, but it will be either migrated or scrapped very soon!

Have a look at the new "Getting Started" section [here](https://fluxml.ai/Flux.jl/dev/).

## Tutorials section

The new (and different than the one I imagined) "Getting Started" prompted a discussion on revamping the existing "Tutorials" section present on `FluxML`'s website. This section is currently heavily outdated and is not updated very regularly, which often misguides or scares newcomers.

We are planning to migrate these tutorials to `Flux`'s documentation to keep them up-to-date using doctests. The contents I initially planned for the new "Getting Started" section are now planned to go into the revamped "Tutorials" section.

Have a look at the new "Tutorials" section [here](https://fluxml.ai/Flux.jl/dev/models/advanced/).

## Independent docs for NNlib.jl

`NNlib` now has standalone docs! `NNlib`'s documentation used to live as an independent page under `Flux`'s documentation, which was not helpful, as `NNlib` is an independent `Julia` package. This was not convenient for both the users and the developers of `NNlib`, as one had to constantly refer to the section in `Flux`'s documentation to get `NNlib` working.

My work here started with migrating the existing page from `Flux`'s documentation to `NNlib`, which was then iterated through helpful reviews! This page was then included in a brand new documentation infrastructure, which was merged way back, but the documentation did not appear live until a few days back. The delay in the deployment of the documentation was caused by a few minor `Documenter.jl` and `DOCUMENTER_KEY` related bugs which have been resolved.

Have a look at `NNlib`'s updated and independent documentation [here](https://fluxml.ai/NNlib.jl).

## Revamped docs for Metalhead.jl

`Metalhead.jl` saw a great amount of development this summer, thanks to a GSoC project led by [`@theabhirath`](https://github.com/theabhirath) and [`@darsnack`](https://github.com/darsnack). With all of this development, it was required to revamp the old `Publish.jl` infrastructure to a modern `Documenter.jl` infrastructure. This invited numerous discussions from FluxML maintainers, given that both the packages have their ups and downs, but in the end, everyone agreed to migrate `Metalhead`'s docs to `Documenter.jl`.

I aimed for a 1:1 port, not adding any information and not removing any information in the porting process, and the new documentation looks beautiful!

Have a look at `Metalhead`'s revamped documentation [here](https://fluxml.ai/Metalhead.jl/dev/index.html).

## Better community health

I have noticed that `Julia`'s ecosystem can be a bit daunting for new contributors because of the missing "Community Health" files. Most of the repositories under `FluxML` lacked issue and PR templates, making the review and triage process harder than it should be. `FluxML` also lacked an organization-wide README, recently introduced by GitHub.

`FluxML` now has default issues and PR templates, which can be overridden by every repository! The organization-wide README is also in its place, guiding newcomers better than ever!

Have a look at the default issue templates [here](https://github.com/FluxML/Flux.jl/issues/new/choose).

Have a look at the organization-wide README [here](https://github.com/FluxML).

Create a PR in a repository under `FluxML` to see the default PR template 😉

## Better docs for OneHotArrays.jl

`Flux.jl` maintainers recently decided to move the "One Hot Encoding" functionalities of `Flux` into a separate independent package. As you might have guessed, this called for some documentation audits!

I have updated and added the docstrings of the `OneHot*` structs to `OneHotArray`'s manual, making them accessible to the users. I also debugged and helped to build the missing `v0.1.0` documentation of `OneHotArrays.jl`!

Have a look at `OneHotArray`'s `v0.1.0` documentation [here](https://fluxml.ai/OneHotArrays.jl).

## Migrating FluxML's website to Franklin.jl

`Franklin.jl` is a modern static site generator written in `Julia`! Quoting their documentation -

> Franklin is a simple, customisable static site generator oriented towards technical blogging and light, fast-loading pages.

`FluxML` maintainers decided to port the existing `FluxML` website (built using `Jekyll`) to `Franklin`, and this was primarily carried out by [`@logankilpatrick`](https://github.com/logankilpatrick) and [`@darsnack`](https://github.com/darsnack). Where do I come in? I helped set up the infrastructure of the new site! I primarily worked on enabling PR previews using GitHub Actions, something not documented in `Franklin`'s documentation (and has not been done before). I also fixed some minor bugs revolving around relative paths and production deployment!

Have a look at the migrated website [here](https://fluxml.ai).

## Adding a new section to Franklin.jl's docs 😉

Referring to the section above, I decided to update `Franklin.jl`'s documentation to include a section on deploying PR previews using GitHub Actions. This eliminated the need for extra infrastructure and also lead to restructuring the original "deploy" documentation of `Franklin`. The revamped "deploy" documentation provides much more options to a user and is easier to navigate through.

I also took the liberty to update outdated documentation of `Franklin`, including outdated GitHub Actions and variable definitions!

Have a look at the revamped deployment page [here](https://franklinjl.org/workflow/deploy/).

## Misc

I cannot possibly think of writing this section without missing out on something. I worked extensively on miscellaneous issues, not limited only to `Flux.jl`, but also related to `FluxML` as a whole. These miscellaneous issues ranged from refining existing `FluxML`'s logos to developing and fixing CI/CD pipelines of `FluxML` packages.

Additionally, while working with `Franklin.jl`, I discovered that `Julia`'s website is open-source and written in `Franklin`! I took this opportunity to update some outdated Actions and syntax on the website. Currently, I am also looking at migrating Julia's website to the new GitHub Pages infrastructure, or the new PR preview infrastructure (mentioned in the section above).

Refer to my GitHub for all the "misc" work carried out by me during the past six months 🙂

## Minor code contributions 😉

Surprisingly, I also contributed to `Flux`'s code. The code contributions weren't in the form of feature additions, instead, I worked on minor bugs and refined the public API.

For instance, I deprecated `rng_from_array()` in the favor of `default_rng_value()`, and then marked it as `@non_differentiable`. These contributions weren't too big, but adding code to `Flux`'s repository did feel good. I look forward to writing more code for `FluxML` in the future!

## Final words

I will be forever grateful to the whole FluxML community for giving me such a wonderful time! I do feel like I have accomplished a bit in the last 6 months, and the documentation of FluxML is at a better place than the point when I started.

A special thanks to [`@DhairyaLGandhi`](https://github.com/DhairyaLGandhi), [`@ToucheSir`](https://github.com/ToucheSir), [`@mcabbott`](https://github.com/mcabbott), and [`@darsnack`](https://github.com/darsnack) for bearing with me through my untidy PRs and helping me out as always!

Oh, I also joined FluxML's GitHub organisation a few weeks back! 🥳

## Tweets

Follow me on Twitter :)

{% twitter https://twitter.com/saranshchopra7/status/1581569050555330560 %}

---

## Appendix
### PRs and issues
Either I created these PRs/issues, or I had some significant involvement in them 😄
#### Flux.jl
- [Fix the last remaining 404 errors](https://github.com/FluxML/Flux.jl/pull/2035)
- [Better docs for reexported packages](https://github.com/FluxML/Flux.jl/pull/2046)
- [Leftover changes from #2046](https://github.com/FluxML/Flux.jl/pull/2055)
- [Add a dark mode version of logo](https://github.com/FluxML/Flux.jl/pull/2063)
- [Fix a few crossrefs + update Zygote's page](https://github.com/FluxML/Flux.jl/pull/2064)
- [Make rng_from_array non differentiable](https://github.com/FluxML/Flux.jl/pull/2065)
- [Back to create_bias](https://github.com/FluxML/Flux.jl/pull/2081)
- [Add GH action format check files with JuliaFormatter](https://github.com/FluxML/Flux.jl/pull/2074)
- [@autosize does not work with semi-colon separated kwargs](https://github.com/FluxML/Flux.jl/issues/2086)
- [Discussion: documentation for @reexported and imported (or using) packages](https://github.com/FluxML/Flux.jl/issues/2038)

#### Metalhead.jl
- [Migrate docs to Documenter.jl](https://github.com/FluxML/Metalhead.jl/pull/199)

#### NNlib.jl
- [Add minimal infrastructure for the docs](https://github.com/FluxML/NNlib.jl/pull/431)
- [Create root level index.html](https://github.com/FluxML/NNlib.jl/pull/438)
- [Trigger tagbot on issue comments](https://github.com/FluxML/NNlib.jl/pull/440)
- [Create independent documentation for NNlib.jl?](https://github.com/FluxML/NNlib.jl/issues/430)

#### OneHotArrays.jl
- [minor doc additions and fixes](https://github.com/FluxML/OneHotArrays.jl/pull/18)
- [Missing v0.1.0 docs + add docs URL in About section](https://github.com/FluxML/OneHotArrays.jl/issues/19)

#### fluxml.github.io
- [Use the latest API of MLDatasets.MNIST](https://github.com/FluxML/fluxml.github.io/pull/146)
- [Use relative folder paths instead of root paths to fix previews](https://github.com/FluxML/fluxml.github.io/pull/154)
- [Port website to Franklin.jl](https://github.com/FluxML/fluxml.github.io/pull/145)
- [Discussion: Update and periodically test posts and model-zoo tutorials](https://github.com/FluxML/fluxml.github.io/issues/141)

#### Franklin.jl
- [New section on previews using GH Actions + update outdated deployment workflows](https://github.com/tlienart/Franklin.jl/pull/982)
- [Rendering and deploying previews using GitHub](https://github.com/tlienart/Franklin.jl/issues/980)
- [Indent YAML block](https://github.com/tlienart/Franklin.jl/pull/981)

#### www.julialang.org
- [Update outdated Actions and syntax for variable definition](https://github.com/JuliaLang/www.julialang.org/pull/1760)
- [Use the new github pages deployment workflow](https://github.com/JuliaLang/www.julialang.org/issues/1719)

#### .github
- [Add PR template, README, and contact links](https://github.com/FluxML/.github/pull/3)
- [Discussion: Flesh out FluxML/.github repository](https://github.com/FluxML/.github/issues/2)
