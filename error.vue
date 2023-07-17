<template>
  <h1>{{ error.statusCode }}</h1>
  <h3>{{ error.message }}</h3>
  <button @click="handleError">Clear errors</button>
</template>

<script setup>
const props = defineProps({
  error: Object
})
const error = props.error

console.log('error:', error)

const handleError = () => clearError({ redirect: '/' })
</script>