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
const nombre = ref(null)
const checked = ref(false)
const selected = ref('')

</script>

<template>
  <main>
    <div>
    <h2>Formulaire</h2     >
    
    <form @submit.prevent>
      <div>
        <label for="texte">Texte : </label>
        <input id="texte" type="text" v-model="texte" />
      </div>

      <div>
        <label for="nombre">Nombre : </label>
        <input id="nombre" type="number" v-model.number="nombre" />
      </div>
      <div class="result">
      <h3>Moustaches :</h3>
      <p>Nom : {{ nom }}</p>
      <p>Nombre : {{ nombre }}</p>
    </div>
 
    </form>
    <div>
      <input type="checkbox" id="checkbox" v-model="checked" />
      <p v-if="checked"> la case est coché</p>
    </div>
    <div>Selected: {{ selected }}</div>

    <div>
<select v-model="selected">
  <option disabled value="">Please select one</option>
  <option>A</option>
  <option>B</option>
  <option>C</option>
</select>

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
    
  </div>

    
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
