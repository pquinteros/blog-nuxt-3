<template>
  <div>
    <header>
      <h1>Blog</h1>
      <Navbar/>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      {{ currentYear }}
    </footer>
  </div>
</template>
<script setup>
const currentYear = new Date().getUTCFullYear()
useHead({
  titleTemplate:'%s - Blog',
  bodyAttrs:[
    { class:'text-center' }
  ],
  link:[
    {
      rel: 'stylesheet',
      href:'https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css',
      integrity:'sha384-9ndCyUaIbzAi2FUVXJi0CjmCapSmO7SnpJef0486qhLnuZ2cdeRhO02iuK6FUUVM',
      crossorigin:'anonymous'
    }
  ],
  script:[
    {
      src: 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js',
      integrity: 'sha384-geWF76RCwLtnZ8qwWowPQNguL3RmwHVBC9FhGdlKrxdiJJigb/j/68SIy3Te4Bkz',
      crossorigin: 'anonymous'
      // body: true
    }
  ]
})
useSeoMeta({
  title: 'My Amazing Site',
  ogTitle: 'My Amazing Site',
  description: 'This is my amazing site, let me tell you all about it.',
  ogDescription: 'This is my amazing site, let me tell you all about it.',
  ogImage: 'https://example.com/image.png',
  twitterCard: 'summary_large_image',
})
</script>
<style lang="scss" scoped>
</style>