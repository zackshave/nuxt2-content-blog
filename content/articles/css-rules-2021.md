---
title: CSS Rules! 2021
description: A quick list of the best CSS properties that I learned in 2021.
image: css-logo.png
alt: Weird ASCII art of the title
---

## What can I say, I like CSS

Every year I learn more and more about it, build increasingly interesting and complex layouts with it, and learn about exciting new features coming down th pipeline. I remember thinking about some of this stuff on this list last year and being excited about using it. I'll include a few properties  at the end of this article that will probably hit browsers in 2022, that I am excited about in the same way.

There is really no set criteria for this list, other than that I used it and am excited about. Some of it has been available in browsers for quite a while and solves an everyday problem, other rules would only be used in specialized cases, and just hit browsers recently.

A big part of what inspired this article was the [State of CSS 2021](https://2021.stateofcss.com/) survey. It's a great reference that shows me the areas of CSS I still have to explore and what upcoming features I should learn. I participated in the survey in 2020 and many of the properties on this list I was inspired to learn because of it. I'd highly recommend taking a look at the results from this year, and participating in State of CSS 2022!

### 1) CSS Grid

CSS Grid spec level 1 has been around for a while, but until recently I was worried about browser support. It wasn't until I watched some [Layout Land videos with Jenn Simmons](https://www.youtube.com/c/LayoutLand) that I learned the main features of grid were actually released to almost immediate full browser support in 2017. There was nothing to be worried about so I just dove in. Those Layout Land videos really helped me get up to speed, as well as [CSSGrid.io](https://cssgrid.io/) from Wes Bos. 

I was so inspired that I ended up creating a demo app on [glitch.com](https://zshave-css-grid-complete.glitch.me/) and slideshow on [CodePen](https://codepen.io/zackshave) that I presented to my coworkers to push adoption of Grid at my current job. Check them out below:

<div class="article__embed-wrapper">
  <div class="glitch-embed-wrap" style="height: 486px; width: 100%;">
    <iframe
      allow="geolocation; microphone; camera; midi; encrypted-media"
      src="https://glitch.com/embed/#!/embed/zshave-css-grid-complete?previewSize=100&previewFirst=true&sidebarCollapsed=true"
      alt="zshave-css-grid-complete on Glitch"
      style="height: 100%; width: 100%; border: 0;">
    </iframe>
  </div>
</div>  

<div class="article__embed-wrapper">
  <p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="GRvweMd" data-user="zackshave" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
    <span>See the Pen <a href="https://codepen.io/zackshave/pen/GRvweMd">
    CSS Grid Slideshow</a> by Zack Shave (<a href="https://codepen.io/zackshave">@zackshave</a>)
    on <a href="https://codepen.io">CodePen</a>.</span>
  </p>
  <script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>

### 2) Position: Sticky

Like every front end focused developer, I've probably implemented 100+ different variations of the classic sticky header pattern. At it's simplest, it could be accomplished with `position: fixed`, but what if you need to scroll down before the sticky UI kicks in? Or if you need to "catch" an element halfway down the page and make it stick? This used to take some JavaScript, with calculations on the height of the sticky element and the distance from the top of the browser, or in more recent years, something like the [Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API).

With `position: sticky;` you can now accomplish this classic UI pattern with just a few lines of CSS. One thing I would like to see is some kind of JavaScript event that you could hook into here for more complex sticky behavior, but you can still use Intersection Observer to accomplish this easily in most cases. Overall, a welcome addition to the CSS spec! Check out the simple demo below: 

<div class="article__embed-wrapper">
  <p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="mdBmNxz" data-user="zackshave" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
    <span>See the Pen <a href="https://codepen.io/zackshave/pen/mdBmNxz">
    Simple CSS-Only Sticky Header </a> by Zack Shave (<a href="https://codepen.io/zackshave">@zackshave</a>)
    on <a href="https://codepen.io">CodePen</a>.</span>
  </p>
  <script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>

### 3) Scroll Snap

Scroll snap is something that I think really helps bring an app-like experience to the web. I love the new UI pattern that uses `display: flex;` and `overflow: scroll` to to simply allow items that don't fit in a container to become, allowing the user to scroll horizontally when with their thumb or mouse-wheel to access the hidden items. I think this makes so much more sense than completely changing the interface for a user between desktop and mobile devices. It's also much easier to implement for developers, and much more performant at a time when we're all obsessing over technical SEO. Scroll snap arrived just in time to make this style of UI feel smoother and more native, and I try to use it wherever I can.  

<div class="article__embed-wrapper">
    <p class="codepen" data-height="400" data-default-tab="result" data-slug-hash="oNwLWJm" data-user="zackshave" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
    <span>See the Pen <a href="https://codepen.io/zackshave/pen/oNwLWJm">
    Horizontal Scroll Snap</a> by Zack Shave (<a href="https://codepen.io/zackshave">@zackshave</a>)
    on <a href="https://codepen.io">CodePen</a>.</span>
  </p>
  <script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
</div>

Honorable mentions goes to [aspect ratio](https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio) and fluid typography using [clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp()). Honestly I wanted to write about these two properties as well, but this article is already so long I doubt many people will get through it. 😅

#### Bonus:

Some properties I am excited about trying out in 2022:

1) [Container queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Container_Queries)
2) [Subgrid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Subgrid)
3) [Perspective](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective)









   