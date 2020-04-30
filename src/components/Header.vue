<template>
  <div class="header">
    <!-- Purple Header -->
    <div class="edge-header blue-gradient"></div>

    <!-- Main Container -->
    <div class="container free-bird">
      <div class="row">
        <div class="col-md-8 col-lg-7 mx-auto float-none white z-depth-1 py-2 px-2">

          <!--Naked Form-->
          <div class="card-body">
            <h1 class="h1-responsive"><strong>Vue To Do List App</strong></h1>
            <p class="pb-4">Remember your tasks</p>

            <div class="alert alert-info" role="alert">
              Click on an <strong>Task Item</strong> to delete it.
            </div>
          </div>
          <!--Naked Form-->

        </div>
      </div>
    </div>
    <!-- /.Main Container -->
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
  .header {
    margin-bottom: 20px;
  }
  
</style>
