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
    <About
      v-if="activePage === 0 || activePage === 4"
      :theme="theme"
      :text-color="textColor"
    />
    <Technologies
      v-if="activePage === 1 || activePage === 4"
      :theme="theme"
      :text-color="textColor"
    />
    <Projects v-if="activePage === 2 || activePage === 4"
      :theme="theme"
      :text-color="textColor"
    /> 
    <Contact v-if="activePage === 3 || activePage === 4"
      :theme="theme"
      :text-color="textColor"
    />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import About from './components/About.vue';
import Technologies from './components/Technologies.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    About,
    Technologies,
    Projects,
    Contact
  },
  data() {
    return {
      activePage: 4,
      theme: 'light',
      logo: "cyh.png",
      btn: "btn btn-primary",
      textColor: 'text-dark',
      pages: [
        {
          link: {text: 'About Me', url: 'about.html' },
        },
        {
          link: { text: 'Technologies', url: 'technologies.html' },
        },
        {
          link: {text: 'Projects', url: 'project.html'},
        },
        {
          link: {text: 'Contact Me', url: 'contact.html'},
        },
      ],
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