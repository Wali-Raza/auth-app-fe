<template>
  <div class="form-container">
    <h2>Login</h2>
    <form @submit.prevent="login">
      <input type="text" v-model="username" placeholder="Username" required />
      <input type="password" v-model="password" placeholder="Password" required />
      <button type="submit">Login</button>
    </form>
  </div>
</template>

<script>
// import axios from 'axios';

export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    async login() {
      const credentials = {
        username: this.username,
        password: this.password
      };
      try {
        console.log("credentials--->",credentials);
        
        // const response = await axios.post('http://localhost:8080/login-service/login', credentials);
        // console.log(response.data); // You can handle the response here
      } catch (error) {
        console.error(error); // Handle errors
      }
    }
  }
};
</script>

<style scoped>
/* Same styling as RegistrationForm */
</style>
