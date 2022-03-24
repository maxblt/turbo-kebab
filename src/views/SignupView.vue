<template>
<div class="signup">
  <main class="form-signin">
    <div class="card">
      <div class="card-body">
        <form>
          <h1 class="h3 mb-3 fw-normal text-center">Please sign up</h1>

          <div class="form-group">
            <label>First Name</label>
            <input type="text" class="form-control form-control-lg" placeholder="First name"/>
          </div>

          <div class="form-group">
            <label>Last Name</label>
            <input type="text" class="form-control form-control-lg" placeholder="Last name"/>
          </div>

          <div class="form-group">
            <label>Email address</label>
            <input type="email" class="form-control form-control-lg" placeholder="Email address" />
          </div>

          <div class="form-group">
            <label>Password</label>
            <input type="password" class="form-control form-control-lg" placeholder="Password"/>
          </div>

          <router-link class="w-100 btn btn-lg btn-primary" type="submit" to="/signin" style="background-color: red; border: red">Sign up</router-link>
        </form>
      </div>
    </div>
    <p class="mt-3 mb-3 text-muted text-center">© 2020–2025</p>
  </main>
</div>
</template>

<script>
export default {
  name: "SignupView"
}
</script>

<style>

.signup {
  padding: 2%;
  display: flex;
  align-items: center;
}
.form-signin {
  width: 100%;
  max-width: 450px;
  margin: auto;
}
label. {
  font-weight: 600;
}
</style>
