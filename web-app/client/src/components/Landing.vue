<template>
  <div class="posts">
    <h1>2020 Presidential Election</h1>
    <h3>Are you a Voter or an Admin?</h3>
    <!--span><b>{{ response }}</b></span><br /-->
    <form v-on:submit="isVoter">
      <input type="submit" value="Voter">
      <br>
    </form>

    <br>

    <form v-on:submit="isAdmin">
      <input type="submit" value="Admin">
      <br>
    </form>

    <vue-instant-loading-spinner id='loader' ref="Spinner"></vue-instant-loading-spinner>
  </div>
</template>

<script>
import PostsService from "@/services/apiService";
import VueInstantLoadingSpinner from "vue-instant-loading-spinner/src/components/VueInstantLoadingSpinner.vue";

export default {
  name: "response",
  data() {
    return {
      loginData: {},
      registerData: {},
      registerReponse: {
        data: ""
      },
      loginReponse: {
        data: ""
      }
    };
  },
  components: {
    VueInstantLoadingSpinner
  },
  methods: {
    async isVoter() {
        this.$router.push("home");
    },
    async isAdmin() {
        this.$router.push("adminLogin");
    },
  }
};
</script>
