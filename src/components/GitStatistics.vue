<template>
  <section>
    <span>Neustes Update: {{ commitText }} ({{ commitId }})</span>
  </section>
</template>

<script>
export default {
  data() {
    return {
      commitText: fetch("")
    }
  }
}
</script>

<style scoped>
  section {
    background-color: rgb(100, 150, 255);
  }
</style>