<template>
  <nav :class="[`navbar-${theme}`, `bg-${theme}`, 'navbar', 'navbar-expand-lg']">
    <div class="container-fluid">
      <!-- <img src="../assets/img/cyh.png" alt="Logo" class="navbar-brand" href="#"> -->
      <a
        @click.prevent="navLinkClick(3)"
        :href="'all.html'"
        title="Yoon's Logo"
        ><img v-if="theme === 'light'" src="../assets/img/cyh.png" alt = "Logo" class="navbar-brand" href = "#">
      <img v-else src="../assets/img/cyhlight.png" alt="Logodfsdfs" class="navbar-brand" href="#"></a>
      <!-- <img src="../assets/img/cyhlight.png" alt="Logodfsdfs" class="navbar-brand" href="#"> -->
      <!-- <a class="navbar-brand" href="#">My Vue</a> -->
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li v-for="(page, index) in pages" class="nav-item" :key="index">
          <a 
            class="nav-link"
            :class="{active: activePage === index}"
            aria-current="page"
            :href="page.link.url"
            :title="`This link goes to the ${page.link.text} page`"
            @click.prevent="navLinkClick(index)"
          >{{ page.link.text }}</a>
        </li>
      </ul>
      <form class="d-flex">
        <!-- <button
          :class="`${btn}`"
          @click.prevent="changeTheme()"
        >Toggle</button> -->
        <button
          :class="`${btn}`"
          @click.prevent="onChange()"
        >Toggle</button>
      </form>
    </div>
  </nav>
  

  <!-- <ul class="nav nav-pills nav-fill">
    <li class="nav-item">
      <a class="nav-link active" aria-current="page" href="#">Home</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Tech</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Project</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#">Contact</a>
    </li>
  </ul> -->
</template>

<script>
export default {
  props: ['pages', 'activePage', 'navLinkClick', 'theme', 'logo', 'btn', 'changeTheme'],
  // data() {
  //   return {
  //     theme: 'light',
  //     logo: "cyh.png",
  //     btn: "btn btn-primary"
  //   }
  // },
  // methods: {
  //   changeTheme() {
  //     let theme = 'light';
  //     let logo = "cyh.png"
  //     let btn = "btn btn-primary";
  //     if (this.theme === 'light') {
  //       theme = 'dark';
  //       logo = "cyhlight.png";
  //       btn = 'btn btn-light'
  //     }
  //     this.theme = theme;
  //     this.logo = logo;
  //     this.btn = btn;
  //   }
  // }
  methods: {
    onChange() {
      this.$emit('change-theme');
    }
  }
}

</script>

<style scoped>
  img {
    height: 50px;
  }

  img:hover {
    cursor: pointer;
  }
</style>