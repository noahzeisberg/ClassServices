<template>
  <nav>
    <img src="./assets/logo.png" alt="">
    <div id="navItemWrapper">
      <a href="#overview">Übersicht</a>
      <a @click="toggleModal" href="#">Absenz</a>
    </div>
  </nav>
  <Overview/>

  <Modal v-if="showModal" @close="toggleModal">
      <h1>Test modal</h1>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Reprehenderit consectetur odit temporibus id exercitationem debitis, quisquam ad dolores nesciunt maiores velit qui ex perspiciatis veniam dolore necessitatibus fugiat, dicta blanditiis!</p>
  </Modal>
</template>

<script>
import Modal from './components/Modal.vue'
import Overview from './components/Overview.vue'

export default {
  name: 'App',
  components: {
    Overview,
    Modal
  },
  data() {
    return {
      showModal: false
    }
  },
  methods: {
    toggleModal() {
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

  input[type="text"] {
    border: none;
    border: 2px solid rgb(225, 225, 225);
    padding: 4px 8px;
    border-radius: 6px;
  }

  button {
    border: none;
    border-radius: 8px;
    background-color: rgb(0, 80, 255);
    width: 100%;
    height: 50px;
    transition: ease-in-out 0.3s;
  }

  button:hover {
    background-color: rgb(70, 128, 255);
    transition: ease-in-out 0.3s;
  }
</style>
