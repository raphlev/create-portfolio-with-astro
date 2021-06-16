# 🎨 Portfolio Example

## Using static site builder Astro
https://astro.build/blog/introducing-astro
https://github.com/snowpackjs/astro
https://twitter.com/astrodotbuild
https://www.learnwithjason.dev/ship-less-javascript-with-astro
https://css-tricks.com/newsletter/255-thoughts-on-astro/
https://aseemtaneja.com/why-i-built-my-blog-with-astro/


In Astro, you compose your website using UI components from your favorite JavaScript web framework (React, Svelte, Vue, etc). Astro renders your entire site to static HTML during the build. The result is a fully static website with all JavaScript removed from the final page. No monolithic JavaScript application required, just static HTML that loads as fast as possible in the browser regardless of how many UI components you used to generate it

How does all this relate to CSS though? Well, according to the docs, all styles are scoped to a component and you can then opt-in to creating global styles. So within a file called Title.astro, you could write something like this:

<style>
  /* Scoped class selector within the component */
  h1 {
    font-weight: bold;
  }
</style>

<h1>I have scoped styles</h1>
And that’s it. No importing a ton of dependencies or whatever; Astro does it all for you. I also love that CSS is within the HTML but you don’t have to write weird JavaScript-esque CSS where it’s all CamalCase or any other format than regular ol’ CSS. This, to me, is a huge improvement over all CSS-in-JS things I’ve seen.
But it’s important to note that the styles above will only be applied to the <h1> in that file. If you want to use global styles then you have to opt into them, like this:

<style>
  :global(h1) {
    font-size: 32px;
  }
</style>

<h1>I have global styles</h1>

Also public/global.scss file can contain global class as well.

```
npm i astro
npm init astro
-> select portfolio
```

```
npm i
npm start
```
