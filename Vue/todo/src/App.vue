<template>
  <div id="app">
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {
  },
  data() {
    return {
     todos: [
       {
         id: 1,
         title: "one",
         completed: false
       },
       {
         id: 2,
         title: "two",
         completed: false
       },
       {
         id: 3,
         title: "three",
         completed: false
       }
     ]
    }
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
