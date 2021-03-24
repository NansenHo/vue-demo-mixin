<template>
  <div id="app">
    <Child1 v-if="child1Visible"/>
    <button @click="child1Visible = false">x1</button>
    <Child2/>
    <button>x2</button>
    <Child3/>
    <button>x3</button>
    <Child4/>
    <button>x4</button>
    <Child5/>
    <button>x5</button>
  </div>
</template>

<script>
import Child1 from "./components/Child1"
import Child2 from "./components/Child2"
import Child3 from "./components/Child3"
import Child4 from "./components/Child4"
import Child5 from "./components/Child5"

export default {
  name: "App",
  date() {
    return {
      child1Visible: true
    }
  },
  components: {
    Child1,
    Child2,
    Child3,
    Child4,
    Child5
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
