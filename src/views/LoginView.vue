<template>
  <div class="login">
    <main class="form-signin">
      <div class="card">
        <div class="card-body">
          <form>
            <h1 class="h3 mb-3 fw-normal text-center">Please sign in</h1>

            <div class="form-group">
              <label>Email address</label>
              <input type="email" class="form-control form-control-lg" placeholder="Email address" />
            </div>

            <div class="form-group">
              <label>Password</label>
              <input type="password" class="form-control form-control-lg" placeholder="Password"/>
            </div>

            <div class="checkbox mb-3">
              <label><input type="checkbox" value="remember-me"> Remember me</label>
            </div>

            <router-link class="w-100 btn btn-lg btn-primary" type="submit" to="/signup" style="background-color: red; border: red">Sign in</router-link>
          </form>
        </div>
      </div>
      <p class="mt-3 mb-3 text-muted text-center">© 2020–2025</p>
    </main>
  </div>
</template>

<script>
export default {
  name: "LoginView",
}
</script>

<style>

.login {
  display: flex;
  padding: 2%;
  align-items: center;
}
.form-signin {
  width: 100%;
  max-width: 450px;
  margin: auto;
}
label {
  font-weight: 600;
}
</style>
