<template>
  <div>
    <div class="educationBody">
      <div class="w-75 p-3 mx-auto">
        <h2 class="mt-3">Education</h2>
        <hr>

        <section class="timeline_area section_padding_130">
          <div class="container px-0">
              <div class="row justify-content-center">
                  <div class="col-12 col-sm-8 col-lg-6">
                      <!-- Section Heading-->
                      <div class="section_heading text-center">
                          <!-- <h6>Our History</h6>
                          <h3>A brief stories of our 2 years company journey</h3> -->
                          <div class="line"></div>
                      </div>
                  </div>
              </div>
              <div class="row">
                  <div class="col-12">
                      <!-- Timeline Area-->
                      <div class="apland-timeline-area">
                        <div v-for='school in educationList'>
                          <div class="single-timeline-area">
                            <!-- <div v-if="index%2==0"> -->
                            <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                <p>{{school.tenure}}</p>
                            </div>
                            <div class="row">
                                <div class="col">
                                    <div class="single-timeline-content wow fadeInLeft" data-wow-delay="0.3s"
                                    style="visibility: visible; animation-delay: 0.3s; animation-name: fadeInLeft;">
                                        <div class="timeline-icon" style="background-size: cover;" aria-hidden="true">
                                          <!-- <i class="fa fa-id-card" aria-hidden="true"></i> -->
                                        </div>
                                        <div class="timeline-text">
                                            <h6 class="my-2">{{school.name}}</h6>
                                            <p>{{school.body}}</p>
                                        </div>
                                    </div>
                                </div>
                              </div>
                            <!-- </div> -->

                          </div>
                        </div>

                                <!-- Single Timeline Content
                                <div class="single-timeline-area">
                                    <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                        <p>2020</p>
                                    </div>
                                    <div class="row">
                                        <div class="col-12 col-md-6 col-lg-4">
                                            <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.3s" style="visibility: visible; animation-delay: 0.3s; animation-name: fadeInLeft;">
                                                <div class="timeline-icon"><i class="fa fa-address-card" aria-hidden="true"></i></div>
                                                <div class="timeline-text">
                                                    <h6>Updated 5.0</h6>
                                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12 col-md-6 col-lg-4">
                                            <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.5s" style="visibility: visible; animation-delay: 0.5s; animation-name: fadeInLeft;">
                                                <div class="timeline-icon"><i class="fa fa-archive" aria-hidden="true"></i></div>
                                                <div class="timeline-text">
                                                    <h6>Fixed bug</h6>
                                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12 col-md-6 col-lg-4">
                                            <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.7s" style="visibility: visible; animation-delay: 0.7s; animation-name: fadeInLeft;">
                                                <div class="timeline-icon"><i class="fa fa-address-book" aria-hidden="true"></i></div>
                                                <div class="timeline-text">
                                                    <h6>Reach 1k Users</h6>
                                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                Single Timeline Content
                                <div class="single-timeline-area">
                                    <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                        <p>2020</p>
                                    </div>
                                    <div class="row">
                                        <div class="col-12 col-md-6 col-lg-4">
                                            <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.3s" style="visibility: visible; animation-delay: 0.3s; animation-name: fadeInLeft;">
                                                <div class="timeline-icon"><i class="fa fa-briefcase" aria-hidden="true"></i></div>
                                                <div class="timeline-text">
                                                    <h6>Updated 4.4.0</h6>
                                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12 col-md-6 col-lg-4">
                                            <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.5s" style="visibility: visible; animation-delay: 0.5s; animation-name: fadeInLeft;">
                                                <div class="timeline-icon"><i class="fa fa-desktop" aria-hidden="true"></i></div>
                                                <div class="timeline-text">
                                                    <h6>Fixed bug</h6>
                                                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                Single Timeline Content
                                <div class="single-timeline-area">
                              <div class="timeline-date wow fadeInLeft" data-wow-delay="0.1s" style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInLeft;">
                                  <p>2019</p>
                              </div>
                              <div class="row">
                                  <div class="col-12 col-md-6 col-lg-4">
                                      <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.3s" style="visibility: visible; animation-delay: 0.3s; animation-name: fadeInLeft;">
                                          <div class="timeline-icon"><i class="fa fa-id-card" aria-hidden="true"></i></div>
                                          <div class="timeline-text">
                                              <h6>Updated 4.0</h6>
                                              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                          </div>
                                      </div>
                                  </div>
                                  <div class="col-12 col-md-6 col-lg-4">
                                      <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.5s" style="visibility: visible; animation-delay: 0.5s; animation-name: fadeInLeft;">
                                          <div class="timeline-icon"><i class="fa fa-desktop" aria-hidden="true"></i></div>
                                          <div class="timeline-text">
                                              <h6>Fixed bug</h6>
                                              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                          </div>
                                      </div>
                                  </div>
                                  <div class="col-12 col-md-6 col-lg-4">
                                      <div class="single-timeline-content d-flex wow fadeInLeft" data-wow-delay="0.7s" style="visibility: visible; animation-delay: 0.7s; animation-name: fadeInLeft;">
                                          <div class="timeline-icon"><i class="fa fa-picture-o" aria-hidden="true"></i></div>
                                          <div class="timeline-text">
                                              <h6>Reach 500 Users</h6>
                                              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
                                          </div>
                                      </div>
                                  </div>
                              </div>
                          </div> -->
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
    /* -webkit-box-shadow: 0 0.25rem 1rem 0 rgba(47, 91, 234, 0.125);
    box-shadow: 0 0.25rem 1rem 0 rgba(47, 91, 234, 0.125);
    border: 1px solid red; */
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
.single-timeline-area .single-timeline-content .timeline-icon i {
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

/* .single-timeline-area .single-timeline-content:hover .timeline-icon,
.single-timeline-area .single-timeline-content:focus .timeline-icon {
    background-color: #020710;
}
.single-timeline-area .single-timeline-content:hover .timeline-text h6,
.single-timeline-area .single-timeline-content:focus .timeline-text h6 {
    color: #3f43fd;
} */



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
        educationList: [
          {name: "Singapore Management University", tenure: "2019-2023", image:"../src/assets/smuLogo.jpg", body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."},
          {name: "La Martiniere for Girls, Kolkata", tenure: "2004-2019", image:"../src/assets/lmgLogo.jpg", body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."}
        ],

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

        // const langTab = document.getElementsByClassName("languageTable");
        // console.log(langTab);

        const divList = document.getElementsByClassName("single-timeline-content");
        for (let i = 0; i < divList.length; i++) {

          var icon = divList[i].getElementsByClassName("timeline-icon")[0];
          icon.style.backgroundImage = 'url('+this.educationList[i].image+')';

          if(i%2==0){
            divList[i].style.backgroundColor = "#B4DAB4";
          }
          else {
            divList[i].style.backgroundColor = "#B4B4DA";
          }
        }


        let width = screen.width;


    }
  }
</script>
