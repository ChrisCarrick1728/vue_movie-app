<template>
  <div id="app">
    <div class="loginContainer">
      <div class="loginHeader">
        <h3>Please Sign in:</h3>
      </div>
      <div class="loginInput">
        <input type="text" name="logon_username" value="" v-model="logon_username" placeholder="User Name...">
        <input type="password" name="logon_password" value="" v-model="logon_password" placeholder="Password...">
        <input type="button" name="submit" value="Login" v-on:click="validateLogon">
        <p>Or</p>
        <input type="button" name="signup" value="Sign up" v-on:click="$emit('swapLogin')">
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      logon_username: '',
      logon_password: ''
    }
  },
  methods: {
    validateLogon: function() {
      console.log("login attempted");
    }
  }
}
</script>

<style>
.loginContainer {
  width: 90%;
  max-width: 300px;
  margin-top: 50px;
  margin-left: auto;
  margin-right: auto;
  background-color: white;
}

.loginHeader h3 {
  font-family: sans-serif;
  font-weight: lighter;
  text-indent: 10px;
  padding: 10px 0px;
  border-bottom: 1px solid #333;
}

.loginInput p, .signupInput p {
  font-family: sans-serif;
  font-weight: lighter;
  text-align: center;
  font-size: 12px;
}

.loginInput input {
  width: 100%;
  height: 30px;
  margin: 10px 0px;
  border: none;
  padding: 0px;
  text-indent: 10px;
}

input:focus {
  outline: none;
  background-color: LightBlue !important;
}

.loginInput input[type=button]{
  background-color: #ccc;
  font-size: 16px;
  cursor: pointer;
}

.loginInput input[type=button]:hover {
  background-color: LightBlue;
}
</style>
