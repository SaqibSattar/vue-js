<script>
export default {
  name: 'App',
  data() {
    return {
      userName: 'Saqi',
      greet: 'Hi',
      website: 'Youtube'
    }
  }
}
</script>
// two ways to bind text // 1. mustache syntax // 2. v-text attribute
<template>
  <div class="wrapper">
    <div>{{ greet }}, {{ userName }}</div>
    <div v-text="website"></div>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
