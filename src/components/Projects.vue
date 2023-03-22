<template>
  <div class="container project-container">
    <h1>Projects</h1>
    <div class="row justify-content-around">
      <div v-for="(project, index) in projects" class="wrapper" :key="index">
        <img v-if="index === 0" src="../assets/img/sr_side_img.png" :alt="project.name" class="proj-one">
        <img v-else-if="index === 1" src="../assets/img/sr_side_img.png" :alt="project.name" class="proj-two">
        <img v-else src="../assets/img/jr_proj_img.png" :alt="project.name" class="proj-three">
        <h4 class="me-2">{{ project.name }} </h4><span> <a href="https://yoonhcho.github.io/Anime-desu/" target="_blank" >Live</a> </span>|<span><a href="https://github.com/YoonHCho/Anime-desu" target="_blank">Code</a></span>
        <p>{{ project.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          name: '3-in-1',
          type: 'Full-Stack',
          live: '',
          code: 'https://github.com/YoonHCho/personal-project',
          description: "A Full-Stack Web Application where users can play a game of Hangman, use Pomodoro to set study time, and write a message. Users can also edit and delete their messages.",
          img: '',
          gif: '',
        },
        {
          name: 'Travel-Map-Journal',
          type: 'Full-Stack',
          live: 'https://travel-map-journal.yoonhc.com/',
          code: 'https://github.com/YoonHCho/travel-map-journals',
          description: "A full stack web application for travel lovers who wants to save the places they've visited: enter journal entry and upload pictures.",
          img: '../assets/img/sr_side_img.png',
          gif: '../assets/img/sr_side_gif.gif',
        },
        {
          name: 'Anime-Desu',
          type: 'Front',
          live: 'https://yoonhcho.github.io/Anime-desu/',
          code: 'https://github.com/YoonHCho/Anime-desu',
          description: "A web application for Anime beginners who wants to get Anime information.",
          img: '../assets/img/jr_proj_img.png',
          gif: '../assets/img/jr_proj_gif.gif',
        }
      ]
    }
  },
}
</script>

<style scoped>
  .project-container {
    width: 65%;
  }

  .wrapper {
    width: 300px
  }

  img {
    max-width: 300px;
  }

  h4 {
    display: inline-block
  }

  @media only screen and (max-width: 992px) {
    .project-container {
      width: 90%;
    }
  }

/* @media only screen and (min-width: 1200px) {
    .contact-container {
      width: 40%;
    }
  } */
  
</style>