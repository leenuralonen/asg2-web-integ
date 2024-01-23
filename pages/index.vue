<script setup>
const { data: hello } = await useFetch("/api/hello");

const clientSideExample = "Updated Blah";
</script>

<template>
  <main>
    <header>
      <h1>Test</h1>
    </header>

    <section>
      <h2>TEstinggggg</h2>
      <p>{{ hello.hello }}</p>
      {{ clientSideExample }}
    </section>
    <section>
      <h2>ayoooowhat</h2>
      <ul>
        <li v-for="character in characters.data" :key="character.id">
          <h3>{{ character.name }}</h3>
          <img :src="character.imageUrl" />
        </li>
      </ul>
    </section>
  </main>
</template>