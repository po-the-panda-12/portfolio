<template>

  <div class = "aboutBody">

    <div class="py-4 px-5 col">

      <h2>About</h2>
      <hr>
      <div class="row">
        <p class="col-sm-8">I am a final year Information Systems undergraduate
          from Singapore Management University (SMU),
          with an interest in Software Development.
          I am passionate about technology and using it to solve problems,
          including my own. Check out my projects below!</p>

        <img src="@/assets/Profile.jpg" alt="profile picture" class="mx-auto">

      </div>

        <a href = "src/assets/CV.pdf" target="_blank"
        class = "btn btn-primary mt-2" download = "Shambhavi Goenka.pdf">
        <i class="fa-solid fa-download"></i>
        Downoad</a>

    </div>

  </div>
</template>


<script>
  export default {
    name: "about"
  }
</script>


<style>

* {
  margin: 0;
  padding: 0;
}

.aboutBody {
  background-color: #2B3A55;
  color: whitesmoke;
}

h2 {
  font-family: "Arvo";
}

img {
  width: 114px;
  height: 100%;
  /* height: 114px; */
}

</style>
