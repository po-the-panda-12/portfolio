<template>

  <div v-for='item in projectList'>

    <div class="row">

      <div class="col">
        <h4 class="my-2">{{item.scope}}</h4>
      </div>

    </div>


      <div class="row">
        <div v-for='project in item.projects' class="col-lg-3 col-md-4 col-sm-6">
          <div class="card my-3">
            <div class="card-body">
              <h5 class="card-title">{{project.title}}</h5>
              <p class="card-text">{{project.summary}}</p>
              <a :href=[project.link] target="_blank" class="btn btn-outline-secondary" id="githubButton" rel="noopener noreferrer">
                <i class="fa-brands fa-github" aria-hidden="true"></i>
                Github</a>
            </div>
          </div>
        </div>
      </div>


  </div>


</template>


<script>
  export default {
    name: "project",

    data() {
      return {
        projectList: [
          {scope: "Machine Learning", projects:[{title:"Image to Text", link:"#", summary:"Extracting license plate numbers from images of cars"}, {title:"Text Generation", link:"https://github.com/po-the-panda-12/shakespearean_text", summary:"Generating Shakesperean text from corpus"}, {title:"Digit Recognition", link:"https://github.com/po-the-panda-12/Digit-Recognition", summary:"Handwritten digit classification with over 97% accuracy"}]},
          {scope: "Web Development", projects:[{title:"Dog dating website", link:"https://github.com/po-the-panda-12/DogPals", summary:"Some content"}, {title:"Something 2", link:"#", summary:"Some content"}]},
          {scope: "Data Analytics", projects:[{title:"Something 3", link:"#", summary:"Some content"}, {title:"Something 4", link:"#", summary:"Some content"}]}
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

#githubButton {
  color: #CE7777;
  border-color:#CE7777;
  font-size:18px;
}

#githubButton:hover {
  background-color: #F2E5E5;
  border-color:#CE7777;
  color: #CE7777;
}


</style>
