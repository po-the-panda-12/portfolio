<template>

  <div class="skillsBody">
    <div class="w-75 p-3 mx-auto">
      <h2 class="mt-3">Languages</h2>
      <hr>
      <div class="row">
        <div v-for='language in languageList' class="col-md-6">
            <p style="width:50%; float:left;">{{language.name}}</p>
            <ul style="width:50%; float:right;">
              <li v-for='index in 5' :key='index'>
                <li v-if='index<=language.rating'>
                  <i class="fa-solid fa-star"></i>
                </li>
                <li v-else>
                  <i class="fa-regular fa-star"></i>
                </li>
              </li>
            </ul>
        </div>
      </div>
    </div>

    <div class="w-75 p-3 mx-auto">
      <h2 class="mt-3">Skills</h2>
      <hr>
      <div class="row">
        <div v-for='skill in skillList' class="col-md-6">
            <p style="width:50%; float:left;">{{skill.name}}</p>
            <ul style="width:50%; float:right;">
              <li v-for='index in 5' :key='index'>
                <li v-if='index<=skill.rating'>
                  <i class="fa-solid fa-star"></i>
                </li>
                <li v-else>
                  <i class="fa-regular fa-star"></i>
                </li>
              </li>
            </ul>
        </div>
      </div>
    </div>
  </div>


</template>

<script>

  export default {
    name: "skills",

    data() {
      return {

        languageList: [
          {name: "Python", rating: "5"},
          {name: "Java", rating: "3"},
          {name: "HTML", rating: "4"}
        ],

        skillList: [
          {name: "Machine Learning", rating: "5"},
          {name: "Web Development", rating: "3"},
          {name: "HTML", rating: "4"}
        ]
      }
    },

    mounted() {

        this.widthAdjust(event);
        window.addEventListener("resize", this.widthAdjust);

    },

    methods: {

      widthAdjust () {
        let width = screen.width;
        var area = document.getElementsByClassName("single-timeline-area");
        var date = document.getElementsByClassName("timeline-date");

        if(width < 575) {
          for (let i = 0; i < area.length; i++) {
            area[i].style.paddingLeft = 0;
            date[i].style.width = 0;
          }
        }
        else {
          for (let i = 0; i < area.length; i++) {
            area[i].style.paddingLeft = "180px";
            date[i].style.width = "180px";
          }
        }
      }
    }
  }

</script>

<style>
@import '@/assets/main.css';

.educationBody {
  padding-top: "40px";
  background-color: #F2E5E5;
  background-size: cover;
}

</style>
