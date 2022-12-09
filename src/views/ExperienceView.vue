<template>
  <div>
    <div class="experienceBody">
      <div class="w-75 p-3 mx-auto">
        <h2 class="mt-3">Experiences</h2>
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
                        <div v-for='school in experienceList'>
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

                                        </div>
                                        <div class="timeline-text">
                                            <h6 class="my-2">{{school.name}}</h6>
                                            <p>{{school.body}}</p>
                                        </div>
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

    <div class="certificationsBody">
      <div class="w-75 p-3 mx-auto">
        <h2>Certifications</h2>
        <hr>
        <ul class="row">
          <li class="col-12">Java Certification</li>
          <li class="col-12">AWS training 1</li>
          <li class="col-12">AWS training 2</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style>

* {
  margin: 0;
  padding: 0;
}

.experienceBody {
  padding-top: 40px;
  background-color: #E8C4C4;
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

.certificationsBody {
  background-color: #2B3A55;
  color: white;
}

h6 {
  font-family: 'opensans-regular', sans-serif;
}



</style>

<script>
  export default {
    name: "ExperienceView",

    data() {
      return {
        experienceList: [
          // {name: "Singapore Management University - TA", tenure: "2019-2023", image:"@/assets/smuLogo.jpg", body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."},
          {name: "Singapore Management University - Main QC", tenure: "2019-2023", image:"@/assets/smuLogo.jpg", body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."},
          // {name: "Singapore Management University - TA", tenure: "2019-2023", image:"@/assets/smuLogo.jpg", body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."},
          {name: "iCompaas - Cyber Sec", tenure: "2004-2019", image:"@/assets/icompaasLogo.jpg", body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."},
          {name: "BIA - DAP", tenure: "2004-2019", image:"@/assets/biaLogo.jpg", body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."}
        ]
      }
    },

    mounted() {

        const divList = document.getElementsByClassName("single-timeline-content");
        for (let i = 0; i < divList.length; i++) {

          var icon = divList[i].getElementsByClassName("timeline-icon")[0];
          icon.style.backgroundImage = 'url('+this.experienceList[i].image+')';

          if(i%2==0){
            divList[i].style.backgroundColor = "#CFD2CF";
          }
          else {
            divList[i].style.backgroundColor = "#F5EDDC";
          }
        }


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
