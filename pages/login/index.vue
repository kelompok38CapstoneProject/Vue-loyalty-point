<template>
  <div class="bg-login">
    <FormLogin />
  </div>
</template>

<script>
export default {
  layout: 'authLayout',
}
</script>

<style>
.bg-login {
  background-image: linear-gradient(to right, #64c2db, #7476ed, #e56f8c);
  height: 100vh;
  position: relative;
}
.login-center {
  margin: 0;
  position: absolute;
  top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}
</style>