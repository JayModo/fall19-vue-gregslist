<template>
  <div class="Job col-4 border rounded">
    <h1>{{jobs.company}}</h1>
    <h5>{{jobs.jobTitle}}</h5>
    <h5>{{jobs.hours}}</h5>
    <h5>{{jobs.rate}}</h5>
    <h5>{{jobs.description}}</h5>

  </div>
</template>
<h2>hello</h2>

<script>
  export default {
    name: 'job',
    props: [],
    data() {
      return {}
    },
    computed: {},
    methods: {
      viewJob() {
        this.router.push({ name: "job", params: { jobId: this.jobProp._id } });
      }
    },
    components: {}
  };
</script>


<style scoped>

</style>