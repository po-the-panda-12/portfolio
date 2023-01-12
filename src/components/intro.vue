<template>

  <div class="homeImage">
    <div class="banner">
      <h1  style="font-size:50px;">Shambhavi Goenka
        <span class = "blink">|</span>
      </h1>
      <p  style="font-size:18px;">AI enthusiast</p>
      <hr>
      <ul>

        <li v-for='ref in refs' class="px-2">
          <a :href=[ref.link] target="_blank" rel="noopener noreferrer">
            <i :class=[ref.icon] aria-hidden="true"  style="font-size:28px;"></i>
          </a>
        </li>

      </ul>
    </div>
  </div>


</template>


<script>
  export default {
    name: "intro",

    data() {
      return {

        refs: [
          {name: "Linkedin", link: "https://www.linkedin.com/in/shambhavi-goenka/", icon: "fa-brands fa-linkedin"},
          {name: "Github", link: "https://github.com/po-the-panda-12", icon: "fa-brands fa-github"},
          {name: "Mail", link: "mailto:shambhavig.2019@scis.smu.edu.sg", icon: "fa-solid fa-envelope"}
        ]
      }
    }

  }
</script>


<style>

* {
  margin: 0;
  padding: 0;
}

h1 {
  font-family: "Arvo";
}


a {
  color: #454545;
  font-size: 30px;
}

a:hover {
    color: #2B3A55;
}

ul li{
  display: inline;
}

.homeImage {
  padding-top: 40px;
  background-image: url("@/assets/HexBack2.jpg");
  background-size: cover;
  height: 100vh;
  width: 100vw;
  text-align: center;
  vertical-align: middle;
  display: table-cell;
}

.banner {
  display: inline-block;
  z-index: 1;
}

.blink {
    animation: blink-animation 1s steps(5, start) infinite;
    -webkit-animation: blink-animation 1s steps(5, start) infinite;
  }

@keyframes blink-animation {
  to {
    visibility: hidden;
  }
}

@-webkit-keyframes blink-animation {
  to {
    visibility: hidden;
  }
}



</style>
