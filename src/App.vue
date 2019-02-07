<template>
  <div id="app">
    <app-header></app-header>
    <component :is="component" v-on:swapLogin="swapLoginComponent"></component>
  </div>
</template>

<script>
import Header from'./components/header.vue';
import Login from './components/login.vue';
import Signup from './components/signup.vue';

export default {
  components: {
    'app-header': Header,
    'app-login': Login,
    'app-signup': Signup
  },
  name: 'app',
  data () {
    return {
      component: 'app-login'
    }
  },
  methods: {
    swapLoginComponent: function() {
      if (this.component == 'app-login') {
        this.component = 'app-signup';
      } else {
        this.component = 'app-login';
      }
    }
  }
}
</script>

<style>
html, body {
  margin: 0px;
}

body {
  background-color: #333;
}
</style>
