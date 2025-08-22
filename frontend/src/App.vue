<template>
  <h1>You did it!</h1>
  <p>
    Visit <a href="https://vuejs.org/" target="_blank" rel="noopener">vuejs.org</a> to read the
    documentation
  </p>

  <div>
    <button @click="fetchData">Fetch Data</button>
  </div>
</template>

<style scoped></style>

<script lang="ts">
export default {
  methods: {
    async fetchData() {
      fetch('/api/alive', {
        referrerPolicy: 'same-origin', // no-referrer-when-downgrade, no-referrer, origin, same-origin...
      })
        .then((res) => res.json())
        .then((data) => {
          debugger
          console.log(data)
        })
    },
  },
}
</script>
