<template>
  <div id="app">
    <div>MyCloud</div>
    <div>
    <button class="loginbutton" @click="loginclick()">Login</button>
    </div>
    <div>
    <button class="loginbutton" @click="signupclick()">회원가입</button>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
import router from "./router/index.js";
export default {
  name: "App",
  methods: {
    loginclick: function() {
      router.push("/login");
    },
    signupclick: function() {
      router.push("/signup");
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.loginbutton {
  background-color: aqua;
  border: none;
}
</style>
