<template>
  <nav :class="[`navbar-${theme}`, `bg-${theme}`, 'navbar', 'navbar-expand-lg']">
    <div class="container-fluid">
      <a
        @click.prevent="navLinkClick(4)"
        :href="'all.html'"
        title="Yoon's Logo"
        ><img v-if="theme === 'light'" src="../assets/img/cyh.png" alt = "Logo" class="navbar-brand" href = "#">
      <img v-else src="../assets/img/cyhlight.png" alt="Logodfsdfs" class="navbar-brand" href="#"></a>
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
        <button
          :class="`${btn}`"
          @click.prevent="onChange()"
        >Toggle</button>
      </form>
    </div>
  </nav>
</template>

<script>
export default {
  props: ['pages', 'activePage', 'navLinkClick', 'theme', 'logo', 'btn', 'changeTheme'],
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

  .navbar-expand-lg {
    border-radius: 10px;
  }
</style>