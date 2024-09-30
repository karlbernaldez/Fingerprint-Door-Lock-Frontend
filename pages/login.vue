<template>
  <div>
    <form @submit.prevent="login">
      <div>
        <label for="email">Email</label>
        <input v-model="email" type="email" id="email" required />
      </div>

      <div>
        <label for="password">Password</label>
        <input v-model="password" type="password" id="password" required />
      </div>

      <button type="submit">Login</button>
    </form>

    <p v-if="errorMessage">{{ errorMessage }}</p>
    <p v-if="successMessage">{{ successMessage }}</p>
  </div>
</template>

<script setup>
import { ref } from "vue";
import axios from "axios";

// Define reactive variables
const email = ref("");
const password = ref("");
const errorMessage = ref("");
const successMessage = ref("");

// Login function
const login = async () => {
  try {
    const response = await axios.post(
      "https://fingerprint-616446599119.asia-south1.run.app/api/auth/login",
      {
        email: email.value,
        password: password.value,
      }
    );

    if (response.status === 200) {
      // Handle successful login
      successMessage.value = "Login successful!";

      errorMessage.value = ""; // Clear any previous error messages
      console.log("Login data:", response.data); // Do whatever is needed after a successful login
    }
  } catch (error) {
    if (error.response && error.response.status === 401) {
      console.log(error.response);
      errorMessage.value = "Incorrect email or password.";
    } else {
      errorMessage.value = "An error occurred. Please try again.";
    }
    successMessage.value = ""; // Clear success message on failure
  }
};

definePageMeta({
  layout: false,
});
</script>
