<template>
  <div :class="[`bg-${theme}`, `${textColor}`, 'container', 'project-container', 'py-3', 'my-3']">
    <h1 class="p-1 mt-1">Projects</h1>
    <div class="row justify-content-around p-1">
      <div class="col-md-5 my-3 py-3 wrapper">
        <img src="../assets/img/per_proj_img.png" :alt="projects[0].name">
        <h4 class="mt-3 me-2 p-2">{{ projects[0].name }} </h4><span><a href="https://github.com/YoonHCho/personal-project" target="_blank">Code</a></span>
        <p class="p-2">{{ projects[0].description }}</p>
      </div>

      <div class="col-md-5 my-3 py-3 wrapper">
        <img src="../assets/img/sr_side_img.png" :alt="projects[1].name">
        <h4 class="mt-3 me-2 p-2">{{ projects[1].name }} </h4><span><a href="https://travel-map-journal.yoonhc.com/" target="_blank" >Live</a> </span>|<span><a href="https://github.com/YoonHCho/travel-map-journals" target="_blank">Code</a></span>
        <p class="p-2">{{ projects[1].description }}</p>
      </div>

      <div class="col-md-5 my-3 py-3 wrapper">
        <img src="../assets/img/jr_proj_img.png" :alt="projects[2].name">
        <h4 class="mt-3 me-2 p-2">{{ projects[2].name }} </h4><span> <a href="https://yoonhcho.github.io/Anime-desu/" target="_blank" >Live</a> </span>|<span><a href="https://github.com/YoonHCho/Anime-desu" target="_blank">Code</a></span>
        <p class="p-2">{{ projects[2].description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['theme', 'textColor'],
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          name: '3-in-1',
          description: "A Full-Stack Web Application where users can play a game of Hangman, use Pomodoro to set study time, and write a message. Users can also edit and delete their messages.",
        },
        {
          name: 'TMJ',
          description: "A Full Stack Web Application for travel lovers who wants to save the places they've visited: enter journal entry and upload pictures.",
        },
        {
          name: 'Anime-Desu',
          description: "A Front End Web Application for Anime beginners who wants to get Anime information.",
        }
      ]
    }
  },
}
</script>

<style scoped>
  .project-container {
    width: 65%;
    border-radius: 10px;
  }

  .wrapper {
    border-radius: 10px;
    background-color: #ca415540;
  }

  img {
    display: block;
    width: 100%;
  }

  .justify-content-around > div:last-child:nth-child(odd) {
    justify-content: flex-start;
  }

  h4 {
    display: inline-block
  }

  a {
    color: #daa45c;
  }

  @media only screen and (max-width: 992px) {
    .project-container {
      width: 90%;
    }
  }
</style>