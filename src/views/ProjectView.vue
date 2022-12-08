<template>
  <div>

    <div class="projectBody">
      <div class="w-75 p-3 mx-auto">
        <h2 class="mt-3" style="color:whitesmoke;">Projects</h2>
        <hr>

        <project />

      </div>
    </div>
  </div>
</template>

<style>

* {
  margin: 0;
  padding: 0;
}

h6 {
  font-family: 'opensans-regular', sans-serif;
}

.projectBody {
  padding-top: 40px;
  background-color: #73838C;
}




</style>

<script>

  import project from '../components/project.vue'

  export default {
    name: "HomeView",
    components : {
            project
        }
  }
</script>
