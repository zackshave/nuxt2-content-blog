---
title: A Vue.js Clock
image: vue-clock.jpg
description: 'A little Vue.js project'
---

## The Inspiration

Earlier this year I took the <a href="https://frontendmasters.com/courses/vue-nuxt-apps/" target="_blank">Building Applications with Vue & Nuxt</a> course on Frontend Masters with Sarah Drasner. It was a great course, with some really interesting projects and very helpful tips along the way. I feel like I came away with a pretty good idea of how to structure a Vue app, in varying level of complexity. One of the beginner projects was a little game with <a href="https://greensock.com/" target="_blank">Greensock</a> animations, and this inspired me to try out something on my own with Vue and Greensock.

## How It Works

Basically when the component loads in VUe, we start a setInterval function that creates a new date object and within that function we update the state that controls each hand of the clock. The state is watched and updates a Greensock rotation value each time it changes. The hardest part was figuring out the math for the hour hand, which to be honest I just found on a math forum.

You can check it out for yourself below:

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="eYRdvvw" data-user="zackshave" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/zackshave/pen/eYRdvvw">
  Simple Vue.js Clock </a> by Zack Shave (<a href="https://codepen.io/zackshave">@zackshave</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


