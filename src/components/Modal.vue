<template>
  <div class="backdrop">
    <div class="modal">
      <slot></slot>
    </div>
  </div>
</template>

<script>

  export default {
    methods: {
      closeSettings() {
        this.$emit("close")
      }
    }
  }
</script>

<style scoped>
  .backdrop {
    width: 100%;
    height: 100%;
    position: fixed;
    display: grid;
    place-items: center;
    top: 0;
    background-color: rgba(0, 0, 0, 0.25);
    backdrop-filter: blur(5px);
  }

  .modal {
    display: flex;
    flex-direction: column;
    justify-content: stretch;
    align-items: stretch;
    overflow: scroll;
    background-color: white;
    width: 25vw;
    border-radius: 16px;
    box-shadow: 0 0 10px 5px rgba(0, 0, 0, 0.25);
    padding: 50px;
  }

  h1 {
    text-align: center;
  }
</style>