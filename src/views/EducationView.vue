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
                      <!-- Timeline Area-->
                      <div class="apland-timeline-area">


                          <div class="single-timeline-area">
                            <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                <p>2019-2023</p>
                            </div>
                            <div class="row">
                                <div class="col">
                                    <div class="single-timeline-content wow fadeInLeft" data-wow-delay="0.3s"
                                    style="visibility: visible; animation-delay: 0.3s; background-color:#B4DAB4; animation-name: fadeInLeft;">
                                        <div class="timeline-icon" style="background-size: cover;" aria-hidden="true">
                                          <img src="@/assets/smuLogo.jpg" alt="logo" class="timeline-icon"></div>
                                        <div class="timeline-text">
                                            <h6 class="my-2">Singapore Management University</h6>
                                            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
                                        </div>
                                    </div>
                                </div>
                              </div>

                          </div>


                          <div class="single-timeline-area">
                            <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                <p>2003-2019</p>
                            </div>
                            <div class="row">
                                <div class="col">
                                    <div class="single-timeline-content wow fadeInLeft" data-wow-delay="0.3s"
                                    style="visibility: visible; animation-delay: 0.3s; background-color:#B4B4DA; animation-name: fadeInLeft;">
                                        <div class="timeline-icon" style="background-size: cover;" aria-hidden="true">
                                          <img src="@/assets/lmgLogo.jpg" alt="logo" class="timeline-icon"></div>
                                        <div class="timeline-text">
                                            <h6 class="my-2">La Martiniere for Girls, Kolkata</h6>
                                            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
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
  </div>
</template>

<style>

* {
  margin: 0;
  padding: 0;
}

.educationBody {
  padding-top: 40px;
  background-color: #F2E5E5;
  background-size: cover;
}

body {
    margin-top: 20px;
}
.timeline_area {
    position: relative;
    z-index: 1;
}
.single-timeline-area {
    position: relative;
    z-index: 1;
    padding-left: 180px;
}
@media only screen and (max-width: 575px) {
    .single-timeline-area {
        padding-left: 100px;
    }
}
.single-timeline-area .timeline-date {
    position: absolute;
    width: 180px;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 1;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -ms-grid-row-align: center;
    align-items: center;
    -webkit-box-pack: end;
    -ms-flex-pack: end;
    justify-content: flex-end;
    padding-right: 60px;
}
@media only screen and (max-width: 575px) {
    .single-timeline-area .timeline-date {
        width: 100px;
    }
}

/* timeline line */
.single-timeline-area .timeline-date::after {
    position: absolute;
    width: 3px;
    height: 100%;
    content: "";
    background-color: black;
    top: 0;
    right: 30px;
    z-index: 1;
}
.single-timeline-area .timeline-date::before {
    position: absolute;
    width: 11px;
    height: 11px;
    border-radius: 50%;
    background-color: #2B3A55;
    content: "";
    top: 50%;
    right: 26px;
    z-index: 5;
    margin-top: -5.5px;
}
.single-timeline-area .timeline-date p {
    margin-bottom: 0;
    color: #020710;
    font-size: 13px;
    text-transform: uppercase;
    font-weight: 500;
}

/* card details */
.single-timeline-area .single-timeline-content {
    position: relative;
    z-index: 1;
    padding: 30px 30px 25px;
    border-radius: 6px;
    margin-bottom: 15px;
    margin-top: 15px;
}
@media only screen and (max-width: 575px) {
    .single-timeline-area .single-timeline-content {
        padding: 20px;
    }
}
.single-timeline-area .single-timeline-content .timeline-icon {
    -webkit-transition-duration: 500ms;
    transition-duration: 500ms;
    width: 60px;
    height: 60px;
    background-color: #2B3A55;
    -webkit-box-flex: 0;
    -ms-flex: 0 0 60px;
    flex: 0 0 60px;
    text-align: center;
    max-width: 60px;
    border-radius: 15%;
    margin-right: 15px;
}
.single-timeline-area .single-timeline-content .timeline-icon img {
    color: #ffffff;
    line-height: 30px;
}
.single-timeline-area .single-timeline-content .timeline-text h6 {
    -webkit-transition-duration: 500ms;
    transition-duration: 500ms;
}
.single-timeline-area .single-timeline-content .timeline-text p {
    font-size: 13px;
    margin-bottom: 0;
}

.single-timeline-content:hover {
  -webkit-box-shadow: 0 0.25rem 1rem 0 rgba(100, 100, 100, 0.125);
  box-shadow: 0 0.25rem 1rem 0 rgba(100, 100, 100, 0.125);
}


h6 {
  font-family: 'opensans-regular', sans-serif;
}

.skillsBody {
  background-color: #CE7777;
  color: white;
}



</style>

<script>
  export default {
    name: "EducationView",

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
