<template>
  <div id="create-Job-modal" class="modal" tabindex="-1" role="dialog">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Create A Job!</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <form @submit.prevent="addJob()">
            <div class="form-group">
              <label for="company">company</label>
              <input type="text" class="form-control" id="company" placeholder="Enter company"
                v-jobTitle="newJob.company" required />
            </div>
            <div class="form-group">
              <label for="jobTitle">jobTitle</label>
              <input type="text" class="form-control" id="jobTitle" placeholder="Enter jobTitle"
                v-jobTitle="newJob.jobTitle" />
            </div>
            <div class="form-group">
              <label for="hours">hours</label>
              <input type="number" class="form-control" id="hours" placeholder="Enter hours"
                v-jobTitle="newJob.hours" />
            </div>
            <div class="form-group">
              <label for="rate">rate</label>
              <input type="number" class="form-control" id="rate" placeholder="Enter rate" v-jobTitle="newJob.rate" />
            </div>


            <div class="form-group">
              <label for="description">Description</label>
              <input type="text" class="form-control" id="description" placeholder="Enter description"
                v-jobTitle="newJob.description" />
            </div>
            <button type="submit" class="btn btn-primary">List Job</button>
          </form>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div>
</template>
<template>
  <div id="create-JobaddJob-modal" class="modal" tabindex="-1" role="dialog">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Create A JobaddJob!</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <form @submit.prevent="addJob()">
            <div class="form-group">
              <label for="make">Make</label>
              <input type="text" class="form-control" id="make" placeholder="Enter make" v-model="newJobaddJob.make"
                required />
            </div>
            <div class="form-group">
              <label for="model">Model</label>
              <input type="text" class="form-control" id="model" placeholder="Enter model"
                v-model="newJobaddJob.model" />
            </div>
            <div class="form-group">
              <label for="year">Year</label>
              <input type="number" class="form-control" id="year" placeholder="Enter year"
                v-model="newJobaddJob.year" />
            </div>
            <div class="form-group">
              <label for="price">Price</label>
              <input type="number" class="form-control" id="price" placeholder="Enter price"
                v-model="newJobaddJob.price" />
            </div>
            <div class="form-group">
              <label for="imgurl">Image Url</label>
              <input type="text" class="form-control" id="imgurl" placeholder="Enter imgurl"
                v-model="newJobaddJob.imgUrl" />
            </div>
            <div class="form-group">
              <label for="description">Description</label>
              <input type="text" class="form-control" id="description" placeholder="Enter description"
                v-model="newJobaddJob.description" />
            </div>
            <button type="submit" class="btn btn-primary">List JobaddJob</button>
          </form>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div>
</template>





<script>
  export default {
    name: 'CreateJobModal',
    data() {
      return {
        newJob: {}
      }
    },
    computed: {},
    methods: {
      addJob() {
        this.$store.dispatch("addJob", this.newJobaddJob);
        this.newJob = {};
      }
    },
    components: {}
  }
</script>


<style scoped>

</style>