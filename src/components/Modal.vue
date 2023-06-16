<template>
  <div class="backdrop">
    <div class="modal">
      <div class="scroll-container">
        <h1>Abwesenheit</h1>
        <div class="divider"></div>
        <h2>Dein Name:</h2>
        <input type="text" id="absenceName">
        <h2>Notizen:</h2>
        <input type="text" id="absenceNote">
      </div>

      <div class="footer">
        <button @click="closeSettings">Schließen</button>
        <button @click="">Abschicken</button>
      </div>
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
  }

  h1 {
    text-align: center;
  }

  .scroll-container {
    display: flex;
    flex-direction: column;
    gap: 16px;
    padding: 35px 75px;
  }

  .divider {
    width: auto;
    height: 2px;
    background-color: rgb(225, 225, 225);
  }

  .footer {
    padding: 32px;
    gap: 32px;
    display: flex;
    justify-content: stretch;
    align-items: center;
  }
</style>