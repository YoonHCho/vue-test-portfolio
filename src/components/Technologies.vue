<template>
  <div :class="[`bg-${theme}`, `${textColor}`, 'container', 'tech-container', 'py-3', 'my-3']">
    <h1 class="p-1 mt-1">Technologies</h1>
    <div class="row p-1 justify-content-between mx-3">
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://reactjs.org/" target="_blank"><img src="../assets/icons/react.svg" alt="react.js"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank"><img src="../assets/icons/javascript.svg" alt="javascript.js"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://nodejs.org/" target="_blank"><img src="../assets/icons/node.svg" alt="node.js"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://expressjs.com/" target="_blank"><img src="../assets/icons/express.svg" alt="express.js"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://www.postgresql.org/" target="_blank"><img src="../assets/icons/postgresql.svg" alt="postgresql"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://developer.mozilla.org/en-US/docs/Glossary/HTML5" target="_blank"><img src="../assets/icons/html5.svg" alt="html5"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://developer.mozilla.org/en-US/docs/Web/CSS" target="_blank"><img src="../assets/icons/css3.svg" alt="css3"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://vuejs.org/" target="_blank"><img src="../assets/icons/vue.svg" alt="vue.js"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://getbootstrap.com/" target="_blank"><img src="../assets/icons/bootstrap.svg" alt="bootstrap"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://cplusplus.com/" target="_blank"><img src="../assets/icons/cplusplus.svg" alt="cplusplus"></a>
      </div>
      <div class="bg-white m-1 py-2 col-5 col-sm-3 col-md-2">
        <a href="https://www.figma.com/" target="_blank"><img src="../assets/icons/figma.svg" alt="figma"></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['theme', 'textColor'],
  name: 'Technologies'
}
</script>

<style scoped>
  .tech-container {
    width: 65%;
    border-radius: 10px;
  }

  .bg-white {
    border-radius: 5px;
    display: inline-block;
  }

  @media only screen and (max-width: 992px) {
    .tech-container {
      width: 90%;
    }
  }
</style>