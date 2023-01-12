<template>

  <div class = "interestBody">

    <div class="py-4 px-5 col">
      <h2>Interests</h2>
      <hr>
      <div class="row" >

        <div v-for='interest in interests'>

          <div class="flip-card my-3 mx-1">
            <div class="flip-card-inner">

              <div class="flip-card-front">
                <table>
                  <tr>
                    <td style="vertical-align:bottom;"><i :class=[interest.icon] aria-hidden="true" class="fa-solid"></i></td>
                  </tr>
                  <tr>
                    <td style="vertical-align:top;"><h6 class="card-title">{{interest.thing}}</h6></td>
                  </tr>
                </table>
              </div>

              <div class="flip-card-back">
                <table>
                  <tr>
                    <td style="vertical-align:middle; color:#F5F5F5;">{{interest.message}}</td>
                  </tr>
                </table>
              </div>

            </div>
          </div>
        </div>

      </div>

    </div>

  </div>
</template>


<script>
  export default {
    name: "interests",

    data() {
      return {

        interests: [
          {thing: "Sports", message: "Especially racquet sports", icon: "fa-person-running"},
          {thing: "Animals", message: "All the furballs", icon: "fa-paw"},
          {thing: "Travel", message: "Always fun to try new food", icon: "fa-plane-departure"},
          {thing: "Hiking", message: "Love the mountains", icon: "fa-mountain-sun"}
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

h2 {
  font-family: "Arvo";
}

.interestBody {
  background-color: #E8C4C4;
}

.flip-card {
  background-color: transparent;
  width: 90px;
  height: 90px;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;

  background-color: #CE7777;
  color: black;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the front side (fallback if image is missing) */
.flip-card-front {
  /* background-color: #CE7777;
  color: black; */
}

/* Style the back side */
.flip-card-back {
  background-color: #995757;
  transform: rotateY(180deg);
}

table {
  height: 100%;
  width: 100%;
}


</style>
