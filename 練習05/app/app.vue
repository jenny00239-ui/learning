<script setup lang="ts">
const count = ref(0)
</script>

<template>
  <main>
    <section class="counter" aria-labelledby="counter-title">
      <p>Nuxt 練習</p>
      <h1 id="counter-title">Count 計數器</h1>
      <output aria-live="polite">{{ count }}</output>
      <button type="button" @click="count++">
        加 1
      </button>
    </section>
  </main>
</template>

<style>
:root {
  font-family: system-ui, sans-serif;
  color: #1f2937;
  background: #f8fafc;
}

body {
  margin: 0;
}

main {
  display: grid;
  min-height: 100vh;
  place-items: center;
}

.counter {
  padding: 2.5rem;
  text-align: center;
  background: white;
  border-radius: 1rem;
  box-shadow: 0 10px 30px rgb(15 23 42 / 12%);
}

p {
  margin: 0;
  color: #64748b;
}

h1 {
  margin: 0.5rem 0 1.5rem;
}

output {
  display: block;
  margin-bottom: 1.5rem;
  font-size: 4rem;
  font-weight: 700;
}

button {
  padding: 0.75rem 1.25rem;
  color: white;
  font: inherit;
  font-weight: 700;
  cursor: pointer;
  background: #2563eb;
  border: 0;
  border-radius: 0.5rem;
}

button:hover {
  background: #1d4ed8;
}
</style>
