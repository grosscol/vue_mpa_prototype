<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-white">
      <a class="navbar-brand" v-bind:href="publicPath">
        <img class="bo-small-logo" width="34" v-bind:src="logo"/>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button> 
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item"><a class="nav-link btn-sm" v-bind:href="publicPath + 'about'">About</a></li>
        </ul>
      </div>
    </nav>
</template>

<script>
import logo from "../assets/bravo_logo_square.png"

export default {
  name: 'NavBar',
  props: { },
  data() {
    return {
      publicPath: process.env.BASE_URL,
      logo: logo
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .bo-small-logo {
    border-radius: 10px;
  }
</style>
