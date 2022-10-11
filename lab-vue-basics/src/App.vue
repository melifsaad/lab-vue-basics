<template>
  <Navbar />
  <div class="separation"></div>
  <h1>APP</h1>

  {{2+2}}
  <br>
  {{sumar()}}
  <br>

  <form>
    <div class="inputName">
      <input v-if="form.name.error" id="input" type="text" placeholder="Name Ok">
      <h2 v-else> Oh no 😢</h2>
      <input id="submit" @submit.prevent="onSubmit()" type="submit" placeholder="submit">
    </div>
  </form>

  <!-- <h1 v-show="ok">Hola!</h1> -->
  <div class="separation"></div>
  <Footer />
</template>

<script setup>
import Navbar from './components/navbar.vue';
import Footer from './components/footer.vue';
import { ref } from 'vue';

const sumar = () => {
  return "Hola Mundo"
}

const form = ref({
  name: {
    content: "",
    error: false
  },
})

const onSubmit = () => {
  console.log(form.value)
  if (form.value.name.content.length === 0) form.value.name.error = true;
  else form.value.name.error = false;
}
</script>

<style scoped>
h1 {
  font-weight: bolder;
}

.inputName {
  height: 80px;
  background-color: #072ac8;
  color: white;
  border: none;
}

.separation {
  background-color: rgb(252, 81, 1);
  padding: 1px;
}
</style>