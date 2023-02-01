<template>
  <NavBar title="NavBar"></NavBar>
    <div id="form">
      <ContactForm title="Contact Form for Yash Ambekar"></ContactForm>
    </div>
    <div class="boot">
    </div>
</template>

<script>
import ContactForm from './components/ContactForm.vue'
import NavBar from "./components/NavBar.vue"

export default {
  name: 'App',
  components: {
    ContactForm,
    NavBar,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
