<template>
  <div id="app">
    {{title}}
    <button class="btn btn-primary" @click="fecthCharacter">Test</button>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      title: "Generate your team"
    };
  },
  methods: {
    fecthCharacter() {
      fetch("https://swapi.co/api/people/?format=json", {
        method: "GET",
      })
        .then(response => response.json())
        .then(json => console.log(json))
    }
  }
};
</script>