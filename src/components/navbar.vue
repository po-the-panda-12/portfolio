<!-- <template>

  <nav class="navbar navbarDefault navbar-expand-sm navbar-dark fixed-top">
    <div class="container">
      <button class="navbar-toggler ml-auto" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <i class="fa-solid fa-bars" style="color:#fff; font-size:28px;"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav mr-auto mb-2 mb-lg-0 center h5">
          <div v-for='item in items'>
            <li class="nav-item px-4">
              <router-link :to="item.link">
                <i :class=[item.icon] aria-hidden="true" class="fa-solid"></i>
                {{item.name}}</router-link>
            </li>
          </div>
        </ul>
      </div>
    </div>
  </nav>

</template>

<style>

* {
  margin: 0;
  padding: 0;
}

body {
  margin-top: 0px !important;
}

.navbar a {
    color: white;
    font-size: 20px !important;
}

.navbarDefault {
  background-color: grey;
}

.navbarScroll {
  background-color: rgba(0,0,0,.3)!important;
}

.navbar-collapse {
  flex-grow: 1;
  text-align: center;
}

.navbar {
  position: relative;

}
.sticky {
  position: sticky;
  top: 0;
}


</style>


<script>

  export default {
    name: "navbar",

    data() {
      return {
        items: [
          {name: "Home", link: "/", icon:"fa-solid fa-house"},
          {name: "Education", link: "/education", icon:"fa-book-open"},
          {name: "Experiences", link: "/experience", icon:"fa-calendar-day"},
          {name: "Projects", link: "/projects", icon:"fa-laptop-code"}
        ]
      }
    },

    created () {
      window.addEventListener('scroll', this.handleScroll);
    },

    destroyed () {
      window.removeEventListener('scroll', this.handleScroll);
    },

    methods: {
      handleScroll (event) {
        var nav = document.getElementsByTagName("nav")[0].classList;
        if(window.pageYOffset > 15) {
          nav.add("navbarScroll");
          nav.remove("sticky");
          nav.add("fixed-top");
        }
        else {
          nav.remove("navbarScroll");
          nav.add("navbarDefault");
          nav.remove("fixed-top");
          nav.add("sticky");
        }
      }
    }
  }


</script> -->


<template>
    <div class="">
      <nav class="navbar navbar-expand-md navbar-dark fixed-top">
        <div class="container-fluid">
          <button class="navbar-toggler ml-auto" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <i class="fa-solid fa-bars" style="color:#fff; font-size:28px;"></i>
          </button>

          <div class="collapse navbar-collapse text-center" id="navbarNav">
            <ul v-for='item in items' class="navbar-nav mr-auto mb-2 mb-lg-0 center h5">

                <li class="nav-item px-4">
                  <router-link :to="item.link">
                    <i :class=[item.icon] aria-hidden="true" class="fa-solid"></i>
                    {{item.name}}</router-link>
                </li>

            </ul>
          </div>

        </div>

      </nav>
    </div>

</template>

<script>
export default {
  name: "navbar",

  data() {
    return {
      items: [
        {name: "Home", link: "/", icon:"fa-solid fa-house"},
        {name: "Education", link: "/education", icon:"fa-book-open"},
        {name: "Experiences", link: "/experience", icon:"fa-calendar-day"},
        {name: "Projects", link: "/projects", icon:"fa-laptop-code"}
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

body {
  margin-top: 0 !important;
}

.navbar a {
    color: whitesmoke;
    font-size: 20px !important;
}

.navbar {
  background-color: rgba(0,0,0,.3)!important;
}



</style>
