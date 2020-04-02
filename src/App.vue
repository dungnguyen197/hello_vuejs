<template>
  <div id="app">
    <img src="./assets/logo.png">
    <button v-on:click="changeTitle">Thay đổi text header</button>
    <h1>{{ msg }}</h1>
    <header-component 
      v-bind:say-hello="sayHello" 
      v-on:handleTitleEvent="handleTitleEvent"/>
    <list-user-component v-bind:list-user="listUser" />
    <footer-component />
  </div>
</template>

<script>
  import HeaderComponent from './components/HeaderComponent.vue'
  import FooterComponent from './components/FooterComponent.vue'
  import ListUserComponent from './components/ListUserComponent.vue'

  export default {
    name: 'app',
    data () {
      return {
        msg: 'Welcome to Your Vue.js App',
        sayHello: 'Hello !',
        listUser: [
          { name: 'dung1', email: 'dung1@gmail.com', active: false },
          { name: 'dung2', email: 'dung2@gmail.com', active: true },
          { name: 'dung3', email: 'dung3@gmail.com', active: true },
        ]
      }
    },
    components: {
      HeaderComponent,
      FooterComponent,
      ListUserComponent
    },
    methods: {
      changeTitle() {
        this.sayHello = 'Hahah';
      },
      handleTitleEvent(data) {
        this.sayHello = data.sayHello;
      }
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
