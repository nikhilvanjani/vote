<template>
  <div class="posts">
    <p>
    <!-- <router-link to="/castBallot">Cast Ballot</router-link>&nbsp; -->
    <router-link to="/QueryAll">QueryAll</router-link>
    </p> 
    <p>
    <router-link to="/queryWithQueryString">Query by Type</router-link>&nbsp;
    <router-link to="/queryByKey">Query by Key</router-link>&nbsp;
    <router-link to="/getCurrentStanding">Get Poll Standings</router-link>&nbsp;
    </p>

    <h1>2020 Presidential Election</h1>
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
    async runSpinner() {
      this.$refs.Spinner.show();
    },
    async hideSpinner() {
      this.$refs.Spinner.hide();
    }
  }
};
</script>
