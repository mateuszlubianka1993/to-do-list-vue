<template>
  <!--Body-->
  <form class="container form-container blue lighten-5">
    <div class="row">
      <div class="col-sm-8">
        <!-- Medium input -->
        <div class="md-form">
          <input v-model="task" type="text" id="inputMDEx" class="form-control" required/>
          <label for="inputMDEx">Add task</label>
        </div>
      </div>
      <div class="col-sm-4 submitButton">
        <button @click.prevent="addNewTask" type="submit" class="btn btn-sm blue-gradient">
          Add
        </button>
      </div>
    </div>
  </form>
</template>

<script>
export default {
    data: function() {
        return {
            task: ''
        }
    },
    methods: {
        addNewTask() {
            this.$emit('taskAdded', this.task);
            this.task = '';
        }
    }
}
</script>

<style scoped>
.submitButton {
    margin: auto;
  }
.form-container {
    max-width: 600px;
    margin-bottom: 15px;
}
</style>
