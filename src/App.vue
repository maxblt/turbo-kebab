<template>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
  <div class="background"></div>
  <nav class="navbar navbar-expand-lg navbar-light" style="background-color: #b3b3b3;">
      <a class="navbar-brand" href="#">Turbo Kebab</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <router-link to="home" class="nav-item nav-link">Home</router-link>
          <router-link to="order" class="nav-item nav-link">Order</router-link>
          <router-link to="signup" class="nav-item nav-link">Sign up</router-link>
          <router-link to="login" class="nav-item nav-link">Log in</router-link>
        </div>
      </div>
    </nav>
  <router-view/>
  <div class="app">

  </div>
</template>

<script>
export default {
  mounted() {
    const plugin1 = document.createElement("script");
    const plugin2 = document.createElement("script");
    plugin1.setAttribute(
        "src",
        "https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"
    );
    plugin2.setAttribute(
        "src",
        "https://code.jquery.com/jquery-3.5.1.slim.min.js"
    );
    plugin1.async = false;
    plugin2.async = false;
    document.head.appendChild(plugin2);
    document.head.appendChild(plugin1);
  }
}
</script>
<style>
a[href="/login"] {
  border: 2px solid black;
}
h1, .navbar-brand {
  font-family: Algerian;
  text-shadow: 2px 2px 8px #000000;
  -webkit-text-stroke: 0.5px red;
  color: white;
}
.background {
  position: fixed;
  left: 0;
  right: 0;
  z-index: -1;
  display: block;
  background-image: url(./assets/turbo-kebab-beautiful.jpg);
  height: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-filter: blur(6px);
  -moz-filter: blur(6px);
  -o-filter: blur(6px);
  -ms-filter: blur(6px);
  filter: blur(6px);
}
</style>
