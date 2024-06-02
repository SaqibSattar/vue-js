<script>
export default {
  name: 'App',
  data() {
    return {
      headingId: 'heading',
      isDisabled: true
    }
  }
}
</script>
// two ways to bind text // 1. mustache syntax // 2. v-text attribute
<template>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
</template>

<style scoped></style>
