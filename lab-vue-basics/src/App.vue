<template>
  <Navbar />
  <div class="separation"></div>
  <h1>APP</h1>
  {{2+2}}
  <br>
  {{Hola()}}
  <br>
  <div v-if="isRender"></div>
  <div v-for="obj in data">{{obj.title}},{{obj.description}},{{obj.content}}</div>
  <div :class="{color: colorChange}">Color</div>
  <button @click="onClick">Click</button>
  <div class="separation"></div>
  <Footer />
</template>

<script setup>
import Navbar from './components/navbar.vue';
import Footer from './components/footer.vue';
import { ref } from 'vue';

const Hola = () => {
  return "Hola Mundo"
}

const isRender = true

const data = [
  {
    title: 'Notebook',
    description: 'Romance',
    content: 'Historia de amor'
  },
  {
    title: 'Guerra de las Galaxias',
    description: 'Ficcion',
    content: 'Mundos'
  },
  {
    title: 'Hannibal',
    description: 'Suspense',
    content: 'Canibalismo'
  }
];

const colorChange = ref(false)
const onClick = () => {
  colorChange.value = !colorChange.value
};

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

.color {
  background-color: red;
}
</style>