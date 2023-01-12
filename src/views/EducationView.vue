<template>
  <div>
    <div class="educationBody">
      <div class="w-75 p-3 mx-auto">
        <h2 class="mt-3">Education</h2>
        <hr>

        <section class="timeline_area section_padding_130">
          <div class="container px-0">
              <div class="row">
                  <div class="col-12">

                      <div class="apland-timeline-area">
                          <div class="single-timeline-area">
                            <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                <p>2019-2023</p>
                            </div>
                            <div class="row">
                                <div class="col">
                                    <div class="single-timeline-content wow fadeInLeft" data-wow-delay="0.3s"
                                    style="visibility: visible; animation-delay: 0.3s; animation-name: fadeInLeft; backgroundColor:#B4DAB4;">
                                        <div class="timeline-icon" style="background-size: cover;" aria-hidden="true">
                                          <img src="@/assets/smuLogo.jpg" alt="logo" class="timeline-icon"></div>
                                        <div class="timeline-text">
                                            <h6 class="mt-3 mb-0">Singapore Management University</h6>
                                            <p class="mb-2" style="font-style:italic; font-size:13px">B.Sc in Software Development and Business Analytics</p>
                                            <p style="font-weight:bold;">Teaching Assistant:</p>
                                            <ul>
                                              <li class="override">Quantum Computing in Financial Services</li>
                                              <li class="override">Corporate Banking and Blockchain</li>
                                            </ul>
                                            <p style="font-weight:bold;">Beyond Curriculars:</p>
                                            <ul>
                                              <li class="override">Business Intelligence & Analytics - Data Associate Program</li>
                                              <li class="override">Coder's Assembly - Mentor</li>
                                            </ul>

                                        </div>
                                    </div>
                                </div>
                              </div>

                          </div>


                          <div class="single-timeline-area">
                            <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                <p>2004-2019</p>
                            </div>
                            <div class="row">
                                <div class="col">
                                    <div class="single-timeline-content wow fadeInLeft" data-wow-delay="0.3s"
                                    style="visibility: visible; animation-delay: 0.3s; animation-name: fadeInLeft; backgroundColor:#B4B4DA;">
                                        <div class="timeline-icon" style="background-size: cover;" aria-hidden="true">
                                          <img src="@/assets/lmgLogo.jpg" alt="logo" class="timeline-icon"></div>
                                        <div class="timeline-text">
                                            <h6 class="mt-3 mb-0">La Martiniere for Girls, Kolkata</h6>
                                            <p class="mb-2" style="font-style:italic; font-size:13px;">Final year results: 96.5/100</p>
                                            <p style="font-weight:bold;">Beyond Curriculars:</p>
                                            <ul>
                                              <li class="override">Computer Club - President</li>
                                              <li class="override">Inter School Swimming</li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                              </div>

                          </div>

                      </div>
                  </div>
              </div>
          </div>
        </section>

        <br/><br/>
      </div>
    </div>


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
              <ul style="width:50%; float:right; display:inline;">
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
  </div>
</template>

<style>
@import '@/assets/main.css';

.educationBody {
  padding-top: 40px;
  background-color: #F2E5E5;
  background-size: cover;
}

.skillsBody {
  background-color: #CE7777;
  color: white;
}

.override {
  display: list-item;
  list-style-position: inside;
}

</style>

<script>
  export default {
    name: "EducationView",

    data() {
      return {

        languageList: [
          {name: "Python", rating: "5"},
          {name: "MySQL", rating: "5"},
          {name: "Javascript (Vue)", rating: "5"},
          {name: "HTML", rating: "5"},
          {name: "Java", rating: "4"}
        ],

        skillList: [
          {name: "Machine Learning", rating: "5"},
          {name: "Data Analytics", rating: "5"},
          {name: "Web Development", rating: "4"},
          {name: "(AWS) Cloud Architecture", rating: "3"}
        ]
      }
    },

    mounted() {

      // const divList = document.getElementsByClassName("single-timeline-content");
      // for (let i = 0; i < divList.length; i++) {
      //
      //   if(i%2==0){
      //     divList[i].style.backgroundColor = "#B4DAB4";
      //   }
      //   else {
      //     divList[i].style.backgroundColor = "#B4B4DA";
      //   }
      // }

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
