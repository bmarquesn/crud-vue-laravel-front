<template>
  <div class="home mt-5">
    <div class="alert alert-success" role="alert" v-if="success">
      {{ success }}
    </div>
    <div class="alert alert-danger" role="alert" v-if="error">
      {{ error }}
    </div>
    <h2 v-if="!user">Welcome, please log in or register</h2>
    <h2 v-else-if="!user.email_verified_at">
      Hello, {{ user.name }}! Registration successful, please check your inbox
      and click confirmation link. If you did not receive the email, click
      <a href="#" @click="verifyResend">here</a> to request another
    </h2>
    <h2 v-else>Hello, {{ user.name }}! You're in.</h2>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";

export default {
  name: "Users",

  data() {
    return {
      success: null,
      error: null
    };
  },

  computed: {

  },

  methods: {

  }
};
</script>
