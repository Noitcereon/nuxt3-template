# nuxt3-template

This is a template I will use for new Nuxt3 projects.

It will include:

- Nuxt3
- TailwindCSS
- TypeScript
- A MainLayout.vue component
- A few example pages

## Installation

1. Scaffold this repository:

Either with De-git or GitHubs "Use this template" feature. Here I use degit:

 ```bash
 npx degit Noitcereon/nuxt3-template your-project-name
 ```
 
 [(what is degit?)](https://github.com/Rich-Harris/degit) 
 
2. Navigate to your-project-name folder 
 ```bash
 cd your-project-folder`
```

3. Make sure to install the dependencies:

```bash
# yarn
yarn install

# npm
npm install

# pnpm
pnpm install --shamefully-hoist
```

4. Initialise git repo (if you want to use Git):
 ```bash
 git init
```

## Usage

This section covers how to start dev server, how to build for production, a link to deployment and some notes about the MainLayout.vue
### Starting Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

### MainLayout.vue

The MainLayout.vue is an alternate way to use layouts, compared to Nuxt's default [(read more aout Nuxt layouts)](https://v3.nuxtjs.org/guide/directory-structure/layouts).

It is used on a page by wrapping the contents of the page in the MainLayout component and providing a the current page as a prop.

Example (prices.vue page):

```
<script lang="ts" setup>
const currentPage = "Prices";
</script>

<template>
  <MainLayout :current-page="currentPage">
    Page: prices
  </MainLayout>
</template>

<style scoped></style>
```

### Production

Build the application for production:

```bash
npm run build
```

Locally preview production build:

```bash
npm run preview
```

Checkout the [deployment documentation](https://v3.nuxtjs.org/guide/deploy/presets) for more information.

## Maintainer
[Noitcereon](https://github.com/Noitcereon)
