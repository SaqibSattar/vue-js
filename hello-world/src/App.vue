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
      isDisabled: true,
      status: 'danger',
      isPromoted: false,
      isSoldOut: true
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

  <!-- Binding Classes -->
  <h2 class="underline">Underlined Text</h2>
  <h2 v-bind:class="status">Status</h2>
  <h2 class="underline" v-bind:class="status">Static Dynamic</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind:class="isSoldOut ? 'sold-out' : 'new'">Soldout? Movie</h2>
  <h2 v-bind:class="['new', 'promoted']">Newly Promoted Movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">
    Array Conditional Movie
  </h2>
  <h2
    v-bind:class="{
      promoted: isPromoted,
      new: !isSoldOut,
      'sold-out': isSoldOut
    }"
  >
    Object Conditional Movie
  </h2>
</template>

<style scoped>
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: olivedrab;
}
.sold-out {
  color: red;
}
</style>
