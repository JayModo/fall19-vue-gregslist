<template>
  <div class="job">
    <h1>{{jobs.company}}</h1>
    <h5>{{jobs.jobTitle}}</h5>
    <h5>{{jobs.hours}}</h5>
    <h5>{{jobs.rate}}</h5>
    <h5>{{jobs.description}}</h5>
  </div>
</template>


<script>

  export default {
    name: 'job',
    data() {
      return {}
    },
    mounted() {
      let payload = {
        jobId: this.$route.params.jobId
      };
      this.$store.dispatch("getJobById", payload);
    },
    computed: {
      job() {
        return this.$store.state.activeJob;
      }
    },
    methods: {},
    components: {}
  }
</script>


<style scoped>

</style>