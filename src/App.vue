<script setup>
import { ref } from 'vue'  

const count = ref(0); 

function increment() {
  count.value++
}

function decrement() {
  count.value--
}

function reset() {
  count.value = 0
}
const texte = ref('')
const age = ref(null)

</script>

<template>
  <main>
    <div class="form-wrapper">
    <h2>Formulaire Vue.js</h2>
    
    <form @submit.prevent>
      <div>
        <label for="texte">Texte : </label>
        <input id="texte" type="text" v-model="texte" />
      </div>

      <div>
        <label for="age">Nombre : </label>
        <input id="age" type="number" v-model.number="age" />
      </div>
    </form>
    <input type="checkbox" id="checkbox" v-model="checked" />
    <label for="checkbox">{{ checked }}</label>
    <input type="checkbox" v-model="toggle" true-value="yes" false-value="no" />
    

    <div class="result">
      <h3>Valeurs saisies :</h3>
      <p>Nom : {{ nom }}</p>
      <p>Âge : {{ age }}</p>
    </div>
  </div>

    <button @click="increment">
      ajouter
    </button>
    <button @click="decrement" :disabled="count ===0" >
      enlever
    </button>
    <button @click="reset">
      reset
    </button>
    <h1>
      {{ count }} 
    </h1>
    


    
  </main>
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
