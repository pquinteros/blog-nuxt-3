<template>
  <div>
    {{ posts[0] }}
    posts...
  </div>
</template>
<script setup>
const { data: posts } = await useFetch('https://jsonplaceholder.typicode.com/posts')
// if (!posts.value) {
//   throw createError({ statusCode: 404, statusMessage: 'Page Not Found' })
// }
</script>