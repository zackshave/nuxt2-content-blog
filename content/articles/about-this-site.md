---
title: About This Site
description: A brief look at the technology behind this site, and my experience developing it.
image: js-mashup.jpg
alt: A crazy mashup of Nuxt, Vue.js, Netlify and JavaScript logos
---

## So what is it?

This site is built with Nuxt.js, using Nuxt/Content as the content management system, deployed on Netlify and using images served from Cloudinary through Nuxt/Image. I'm using Sass to write the styles, and I'm not using a CSS framework. 

## Why?

I decided to revamp my personal site last year and as a fun way to get up to speed on new React frameworks like Gatsby and Next.js. Initially I wanted to make a Gatsby site, because I love their image processing, but I found that even though I have a decent understanding of React, there were a lot of barriers to actually getting data into my components. I needed to add lots of plug-ins and configuration to get what I wanted out of it.

This was especially true in this particular case because I was planning on a very image heavy website, and I wanted to use Cloudinary to accomplish this without paying for extra storage on Github or Netlify. I eventually did figure out a way to combine two Cloudinary Gatsby plugins and some GraphQL mutations to get the images to work they way I wanted, but I was frustrated by the experience. I still plan to finish this project and create a photography website for myself at some point, and when I do so I'll blog about it here.

While I was working on this Gatsby project I did a few crash courses on Vue.js and instantly fell in love with it. It's just so much closer to the web development that I am used to when compared to React, but still offers incredibly powerful features in a progressively scalable way. As I got deeper into the Vue ecosystem I discovered Nuxt and it seemed like a great fit for a personal site deployed on the Jamstack.

   