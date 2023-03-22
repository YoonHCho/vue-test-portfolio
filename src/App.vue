<template>
  <div class="container">
    <Navbar
      :pages="pages"
      :active-page="activePage"
      :nav-link-click="(index) => activePage = index"
      :theme="theme"
      :logo="logo"
      :btn="btn"
      @change-theme="changeTheme"
    ></Navbar>
    <!-- <PageViewer
      :page="pages[activePage]"
    >

      :projects="projects"

    </PageViewer> -->
    <About
      v-if="activePage === 0 || activePage === 3"
      :theme="theme"
      :text-color="textColor"
    />
    <Projects v-if="activePage === 1 || activePage === 3" /> 
    <Contact v-if="activePage === 2 || activePage === 3"
      :theme="theme"
      :text-color="textColor"
    />

  </div>
</template>

<script>
import PageViewer from './components/PageViewer.vue';
import Navbar from './components/Navbar.vue';
import About from './components/About.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    About,
    Projects,
    PageViewer,
    Contact
  },
  data() {
    return {
      activePage: 3,
      theme: 'light',
      logo: "cyh.png",
      btn: "btn btn-primary",
      textColor: 'text-dark',
      pages: [
        {
          link: {text: 'About Me', url: 'about.html' },
          pageTitle: 'Home Page',
          content: 'This is the home content'
        },
        {
          link: {text: 'Projects', url: 'project.html'},
          pageTitle: 'About Page',
          content: 'This is the Project content'
        },
        {
          link: {text: 'Contact Me', url: 'contact.html'},
          pageTitle: 'Contact Page',
          content: 'This is the Contact content'
        },
      ],
      projects: [
        {
          type: 'Full',
          live: '',
          code: 'https://github.com/YoonHCho/personal-project',
          description: "A Full-Stack Web Application where users can play a game of Hangman, use Pomodoro to set study time, and write a message. Users can also edit and delete their messages.",
          img: '',
          gif: '',
        },
        {
          type: 'Full',
          live: 'https://travel-map-journal.yoonhc.com/',
          code: 'https://github.com/YoonHCho/travel-map-journals',
          description: "A full stack web application for travel lovers who wants to save the places they've visited: enter journal entry and upload pictures.",
          img: '../assets/img/sr_side_img.png',
          gif: '../assets/img/sr_side_gif.gif',
        },
        {
          type: 'Front',
          live: 'https://yoonhcho.github.io/Anime-desu/',
          code: 'https://github.com/YoonHCho/Anime-desu',
          description: "A web application for Anime beginners who wants to get Anime information.",
          img: '../assets/img/jr_proj_img.png',
          gif: '../assets/img/jr_proj_gif.gif',
        }
      ]
    };
  },
  methods: {
    changeTheme() {
      let theme = 'light';
      let logo = "cyh.png"
      let btn = "btn btn-primary";
      let textColor = 'text-dark'
      if (this.theme === 'light') {
        theme = 'dark';
        logo = "cyhlight.png";
        btn = 'btn btn-light';
        textColor = "text-white";
      }
      this.theme = theme;
      this.logo = logo;
      this.btn = btn;
      this.textColor = textColor;
    }
  }
}
</script>