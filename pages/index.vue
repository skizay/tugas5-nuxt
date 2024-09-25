<template>
    <!-- BEGIN NAVBAR -->
  <div class="navbar">
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#education">Education</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </div>
    <!-- END NAVBAR -->

    <div class="container">

      <!-- HEADER -->
      <div class="jumbotron">
        <div class="jumbotron-text">
          <h1>Iffah Azzahro</h1>
          <p> Information Technologhy Student </p>
        </div>
        <div class="jumbotron-social">
          <ul class="ul-social">
            <li class="li-social-links">
              <a class="social" href="https://github.com/skizay" target="_blank"><i class="fa fa-github" aria-hidden="true"></i></a>
            </li>
            <li class="li-social-links">
              <a class="social" href="https://www.linkedin.com/in/iffah-az-zahro" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
            </li>
          </ul>
        </div>
        <div id="down-arrow">
          <span><a href="#about"><i class="fa fa-chevron-down" aria-hidden="true"></i></a></span>
        </div>
      </div>
      <!-- END HEADER -->

      <!-- BEGIN ABOUT -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="about"></a>
            <h2>About</h2>
          </div>
          <div class="content-body">
            <p>Hi there 👋! I'm iffah </p>
            <p>I'm a third-year information technologhy student from Brawijaya University currently studying web development, mobile development, artificial intellegence and computer network. My dream is to work for google or any tech company around the world one day.
                I love design and still learning on it to become a profesional designer one day! I also like travelling to keep sane. Totally hippie lol ✌️.</p>
            <p>Welcome to my portfolio!</p>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END ABOUT -->

      <!-- BEGIN EXPERIENCE -->
      <div class="row">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="experience"></a>
            <h2>Experience</h2>
          </div>
          <!-- CARD #1 -->
          <div class="content-body">
            <div class="card" v-for="experience in experiences">
              <div class="card-header">
                <h4>{{experience.company}} <span class="job-title">{{experience.job_title}}</span></h4>
              </div>
              <div class="card-content">
                <p>{{ experience.description }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END EXPERIENCE -->

      <!-- BEGIN EDUCATION -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="education"></a>
            <h2>Education</h2>
          </div>
          <div class="content-body">

            <!-- EDUCATION DATA -->
            <div class="card" v-for="education in educations">
              <div class="card-header">
                <h4>{{education.name}} <span class="job-title">{{education.date_attended}}</span></h4>
              </div>
              <div class="card-content">
                <!-- baru deh disini dipanggil si description tadi --> 
                <p>{{ education.description }}</p>
              </div>
            </div>

          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END EDUCATION -->

      <!-- BEGIN PROJECTS -->
      <div class="row">
        <div class="side-content-sm"></div>
        <div class="main-content-lg">
          <div class="content-header">
            <a class="anchor" name="projects"></a>
            <h2>Projects</h2>
          </div>
          <div class="content-body">
            <!-- CARD #1 -->
            <div class="project-card" v-for="project in projects">
              <div class="project-content">
                <h4>{{project.project_name}}</h4>
                <a :href="project.link">Project repository</a>
                <p></p>
              </div>
            </div>
          </div>
        </div>
        <div class="side-content-sm"></div>
      </div>
      <!-- END PROJECTS -->

      <!-- BEGIN SKILLS -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="skills"></a>
            <h2>Skills</h2>
          </div>
          <div class="content-body">
            <ul class="ul-skills">
              <li class="li-skills" v-for="skill in skills">{{ skill }}</li>
            </ul>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END SKILLS -->

      <!-- BEGIN FOOTER -->
      <div class="row">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
          </div>
          <div class="content-body">
            <p>Copyright Iffah 2024</p>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END FOOTER -->
    </div>
</template>
<style>
@import url("~/assets/style.css");
</style>

<script>
export default {
  data(){
    return{
      // Data Personal
      skills: ["HTML", "Javascript", "PHP", "Vue", "Python"],

      educations: [
        {name: "Brawijaya University", date_attended:"2023 - 2026", description:"Information technologhy student at Brawijaya University "},
        {name: "Antartika Senior High School", date_attended:"2020 - 2023", description:"Graduated in Natural Science"}, 
      ],

      experiences: [
        {company: "PT. Telkom Indonesia", job_title: " Intership ", description:" 3 months internship as project assistant "},
        {company: "Tokopedia ", job_title: " Internship ", description:" 3 months internship as software engineering"},
      ],

      projects: [
        {project_name: "Color change, Increment, Carousel using Vue JS", description: "", link: "https://github.com/skizay/Vue-app"},
        {project_name: "Contactform using PHP", description: "", link: "https://github.com/skizay/Contact-Form"},
      ]
    }
  }
}
</script>