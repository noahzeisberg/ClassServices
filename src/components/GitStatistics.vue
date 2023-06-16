<template>
  <section>
    <span><strong>Neustes Update:</strong> {{ commitText }} (<a href="">{{ commitId }}</a>)</span>
  </section>
</template>

<script>
export default {
  data() {
    return {
      commitText: "Statussektion wurde hinzugefügt.",
      commitId: "#297dc28"
    }
  }
}
</script>

<style scoped>
  section {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 6px 12px;
    background-color: rgb(225, 225, 225);
  }

  a {
    color: black;
    text-decoration: underline;
  }
</style>