# Style Rendered Markdown using Tailwind Typography

You can use the `@tailwindcss/typography` plugin to style rendered Markdown from sources such as Astro's [**content collections**](https://docs.astro.build/en/guides/content-collections/).

## Setting Up `@tailwindcss/typography`

First, install `@tailwindcss/typography` from `npm` using your preferred package manager.

```bash
npm install -D @tailwindcss/typography 
```

Then, add the package as a plugin within your Tailwind configuration file.

```diff lang="js"
// tailwind.config.js
/** @type {import('tailwindcss').Config} */

module.exports = {
  theme: {
    // ...
  },
  plugins: [
+   require('@tailwindcss/typography'),
    // ...
  ],
}
```

## Using `@tailwindcss/typography`

`@tailwindcss/typography` uses **element modifiers** to style child components of a container with the `prose` class. These modifiers follow the general syntax of `prose-[element]:class-to-apply`. For example, `prose-h1:font-bold` would be used to give all `<h1>` tags the `font-bold` Tailwind class.

## Recipe

1. Create a `<Prose>` component to encapsulate your rendered Markdown. 

```astro
// src/components/Prose.astro
---
---
<div class="prose dark:prose-invert prose-h1:font-bold prose-h1:text-xl prose-a:text-blue-600 prose-p:text-justify prose-img:rounded-xl prose-headings:underline mx-auto">
  <slot />
</div>
```

2. Then, use the `<Prose>` component as a parent for your Markdown. If you are using **content collections**, your code might look like this:

```astro
// src/pages/index.astro
---
import Prose from "../components/Prose.astro";
import Layout from "../layouts/Layout.astro";
import { getEntry } from 'astro:content';

const entry = await getEntry('collection', 'entry');
const RenderedMarkdown = await entry.render();
---
<Layout>
  <Prose>
    <RenderedMarkdown />
  </Prose>
</Layout>
```

You can view a live example of this recipe <a href="https://stackblitz.com/edit/withastro-astro-scvyma?file=src%2Fpages%2Findex.astro" target="_blank">here on StackBlitz</a>