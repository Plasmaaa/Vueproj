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
    <div>watchers
      <input type="(ref)">
    </div>
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
