<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'Saqi',
      greet: 'Hello',
      channel: '<b>Youtube</b>',
      hack: `<a href="#" onclick="alert('You have been hacked!')">Win a prize!<a/>`,
      headingId: 'heading',
      isDisabled: true
    }
  }
}
</script>

// two ways to bind text // 1. mustache syntax // 2. v-text attribute

<template>
  <!-- Binding Text -->
  <div>{{ greet }} {{ name }}</div>

  <!-- Binding HTML -->
  <div v-html="channel"></div>
  <div v-html="hack"></div>

  <!-- Binding Attributes -->
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
</template>

<style scoped></style>
