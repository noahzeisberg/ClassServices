<template>
  <nav>
    <img src="./assets/logo.png" alt="">
    <div id="navItemWrapper">
      <a href="#overview">Übersicht</a>
      <a @click="toggleSettings" href="#">Einstellungen</a>
    </div>
  </nav>

  

  <SettingModal v-if="showModal" @close="toggleSettings"/>
</template>

<script>
import SettingModal from './components/SettingModal.vue'

export default {
  name: 'App',
  components: {
    SettingModal
  },
  data() {
    return {
      showModal: false
    }
  },
  methods: {
    toggleSettings() {
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

  * {
    margin: 0;
    padding: 0;
    font-family: 'Poppins';
		font-size: 16.5px;
  }

  body {
    padding: 0;
    margin: 0;
  }

  a {
    text-decoration: none;
  }

  h1 {
    font-size: 32px;
  }

  ::selection {
    background-color: rgb(0, 80, 255);
  }

  #app nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: rgb(0, 80, 255);
    padding: 16px 32px;
  }

  #app nav a {
    color: rgb(215, 234, 243);
  }

	#app nav img {
		width: 35px;
		aspect-ratio: 1;
	}

	#app nav #navItemWrapper {
		display: flex;
		align-items: center;
		gap: 25px;
	}
</style>
