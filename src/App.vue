<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'about' }">About</router-link> |
    <router-link :to="{ name: 'Jobs' }">Jobs</router-link>
  </nav>

    <button @click="back" >Go Back</button>
    <button @click="forward">Go Forward</button>
    <button @click="refresh">Refresh</button>
  <router-view/>

  

</template>

<script>
export default {
  methods: {
    back() {
      this.$router.go(-1);
    },
    forward() {
      this.$router.go(1);
    },
    refresh() {
      this.$router.go(0);
    }
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

::selection {
  background: black;
  color: yellowgreen;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  margin : 10px;
}

nav a.router-link-exact-active {
  color: #42b983;
  background-color: crimson;
  padding: 10px;
  border-radius: 5px;
  color: white;

  /* Remove transition to see if it affects the animation */
  /* transition: all 0.3s; */
}

h1 {
  font-size: 2em;
  text-transform: uppercase;
}


button {
  padding: 10px;
  border-radius: 5px;
  color: white;
  font-weight: bold;
  background-color: crimson;
  border: none;
  cursor: pointer;
  margin: 10px;
}

</style>
