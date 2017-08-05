---
title: Refactoring my way into a design system
date: 2017-07-10 18:08:17 -0500
tags: web design
---
I was inspired by [@aizlewood's](http://twitter.com/aizlewood) recent post about how ["the lowly page is crucial in ensuring a strong, solid design system"](http://jonaizlewood.com/articles/design-systems-dont-start-with-components) to share one small design technique I've figured out while dancing over the line publishing between web *pages* and web *apps*: the simple process of [refactoring](https://en.wikipedia.org/wiki/Code_refactoring) your front end code will end up creating your design system for you.

When first building a website, don't even think about design systems. Don't overthink it, don't over plan it, just build the first page. Put all the CSS into a single file. Who cares.

Then, when (or if!) you need a second page, just start building it. In the course of this you may find something from the first page you want to include in the second. Fantastic! Refactor it into something that can be reused between the two pages: give them a shared class name, pull the CSS into its own file, heck make it a component if you really want to. That's the first entry in your design system.

This is one of the things that designers can learn from the process of coding. The _test ⟳ refactor loop_ was one of the biggest procedural breakthroughs I've made professionally because I learned how to get out of my own way. Just focusing on making the thing work and knowing that I'll get the opportunity to improve the way it works — *if that's even necessary* — at a later date lets me focus on what's essential.

And I think that's what @aizlewood meant by "good design systems start with a vision. A creative direction before they become a thing." Make sure that it works at all before getting caught up in the finicky details of how it's working.