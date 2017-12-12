<template>
  <div class="container mt-10">
    <h3 class="title">John Pham is creating web apps, teaching computer science, and designing.</h3>
    
    <div id="links">
      <a class="link-nav" href="http://linkedin.com/in/johnpham97">linkedin</a>
      <a class="link-nav" href="http://goo.gl/T7TX7j">github</a>
      <a class="link-nav" href="../static/docs/johnpham_resume.pdf">resume</a>
      <a class="link-nav" href="mailto:johnphammail@gmail.com">email</a>
      <a class="link-nav" href="https://goo.gl/7708EP">graphics</a>
      <a class="link-nav" href="../static/calendar.html">calendar</a>
    </div>

    <div class="section">
      <a v-for="p in projects"
        :key="p.name"
        :href="p.projectUrl"
        class="row project"
      >
        <div class="col-md-6">
          <img class="project-image" :src="`../static/projects/${p.imageUrl}`" alt="">
        </div>
        <div class="col-md-6">
          <div class="project-description">
            <h3 class="project-title">{{ p.name }}</h3>
            <p class="text-muted">{{ p.role }}</p>
            <p>{{ p.description }}</p>
          </div>
        </div>
      </a>
    </div>

    <div class="section container">
      <h4 class="section-title text-center">Places I've worked for.</h4>

      <div class="row">
        <div class="col-md-3 offset-md-3 work-container">
          <img class="work-item" src="../static/google.png" alt="Google">
        </div>
        <div class="col-md-3 work-container">
          <img class="work-item" src="../static/aerospace.png" alt="Aerospace Corporation">
        </div>
      </div>
      
      <div class="row">
        <div class="col-md-3 offset-md-2 work-container">
          <img class="work-item work-container" src="../static/nasa-jpl.png" alt="NASA JPL">
        </div>
        <div class="col-md-3 work-container">
          <img class="work-item" src="../static/amazon.png" alt="Amazon">
        </div>
        <div class="col-md-3 work-container">
          <img class="work-item" src="../static/aaf.png" alt="American Advertising Agency">
        </div>
      </div>
    </div>

    <div class="section container">
      <h4 class="section-title text-center">What I've been up to.</h4>
    </div>

  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Roboto:400,600,700');
html, body {
  font-family: 'Roboto', sans-serif;
}
.title {
  width: 50%;
  font-weight: 600;
}
#links {
  margin-bottom: 50px;
}
.section {
  margin-top: 30px;
}
.section-title {
  margin-bottom: 30px;
  font-weight: 600;
}
.mt-10 {
  margin-top: 5vh;
}
.link-nav {
  margin: auto 1em auto 0;
  color: black;
  text-decoration: underline;
}
.project-description {
  margin-top: 20px;
  padding-left: 10px;
}
.project-title {
  font-weight: 600;
}
.project-image {
  width: 100%;
}
.project {
  color: black;
  margin-bottom: 20px;
  -webkit-transition: 1s;
  transition: 1s;
}
.project:hover {
  -webkit-box-shadow: 15px 17px 85px -51px rgba(0,0,0,0.58);
  -moz-box-shadow: 15px 17px 85px -51px rgba(0,0,0,0.58);
  box-shadow: 15px 17px 85px -51px rgba(0,0,0,0.58);
}
.project, a:hover, a:focus {
  text-decoration: none;
}
.work-container {
  align-items: center !important;
  -ms-flex-align: center !important;
  display: flex;
}
.work-item {
  width: 100%;
  vertical-align: middle;
}
</style>

<script>
export default {
  name: 'JohnPham',
  data: function () {
    return {
      projects: [
        {
          name: 'Department of Electrical and Computer Engineering at UC Riverside',
          projectUrl: 'http://ece.ucr.edu',
          imageUrl: 'ece.jpg',
          role: 'Web Developer',
          description: 'Main website used for college admissions and student resources'
        },
        {
          name: 'Video Computing Group',
          projectUrl: 'http://vcg.engr.ucr.edu',
          imageUrl: 'vcg.jpg',
          role: 'Web Developer',
          description: 'Landing page'
        },
        {
          name: 'CSAMBA',
          projectUrl: 'http://csamba.ucr.edu',
          imageUrl: 'csamba.jpg',
          role: 'Lead Web Developer',
          description: 'Landing page and internal assets manager'
        },
        {
          name: 'Grep Jobs',
          projectUrl: 'https://devpost.com/software/pennapps16-grepjobs',
          imageUrl: 'grepjobs.png',
          role: 'Project Lead, Front-end Developer',
          description: 'Won the Best Data Visualization Prize and placed in the Top 10 out of 170 at PennApps'
        }
      ]
    }
  }
}
</script>