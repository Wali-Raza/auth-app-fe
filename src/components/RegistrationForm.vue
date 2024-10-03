<template>
  <div class="form-container">
    <h2>Register</h2>
    <form @submit.prevent="register">
      <input type="text" v-model="username" placeholder="Username" required />
      <input type="email" v-model="email" placeholder="Email" required />
      <input type="password" v-model="password" placeholder="Password" required />
      <button type="submit">Register</button>
    </form>
  </div>
</template>

<script>
// import axios from 'axios';

export default {
  data() {
    return {
      username: '',
      email: '',
      password: ''
    };
  },
  methods: {
    async register() {
      const userData = {
        username: this.username,
        email: this.email,
        password: this.password
      };
      try {
        debugger
        console.log("userData->>>",userData);
        
        //const response = await axios.post('http://localhost:8080/registration-service/register', userData);
        // console.log(response.data); // You can handle the response here
      } catch (error) {
        console.error(error); // Handle errors
      }
    }
  }
};
</script>

<style>
.form-container {
  max-width: 400px;
  margin: auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
input {
  display: block;
  width: 100%;
  margin-bottom: 10px;
  padding: 10px;
}
button {
  width: 100%;
  padding: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
}
</style>
