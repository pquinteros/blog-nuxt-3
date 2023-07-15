<template>
  <div>
    post {{ id }}
  </div>
</template>
<script setup>
const { id } = useRoute().params
definePageMeta({
  validate: async (route) => {
    return /^\d+$/.test(route.params.id)
  } 
})
</script>