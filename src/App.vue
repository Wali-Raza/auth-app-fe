<template>
  <div id="app">
    <h1>User Authentication</h1>
    <RegistrationForm />
    <LoginForm />
  </div>
</template>

<script>
import RegistrationForm from './components/RegistrationForm.vue';
import LoginForm from './components/LoginForm.vue';

export default {
  name: 'App',
  components: {
    RegistrationForm,
    LoginForm
  }
};
</script>

<style>
#app {
  text-align: center;
  padding: 20px;
}

h1 {
  margin-bottom: 20px;
}
</style>
