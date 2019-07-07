<template>
  <div id="app" class="div">
    <!-- using v-text <h1 v-text="name"></h1>
    using v-html <h1 v-html="name"></h1>
    using interpolation <h1>{{name}}</h1> -->

    <homework></homework>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Homework from './components/Homework.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Homework
  },
  data() {
    return {
      name: 'Dhruv Seta',
      list: [
        {
          content: 'First',
          urlId: 55
        },
        {
          content: 'second',
          urlId: 65
        },
        {
          content: 'third',
          urlId: 75
        }
      ]
    }
  },
  method: {
    
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
