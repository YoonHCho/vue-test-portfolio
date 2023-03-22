<template>
  <div :class="[`bg-${theme}`, `${textColor}`, 'container', 'about-container', 'py-3', 'my-3']"
  >
    <h1 class="text-start same-line p-1 mt-1">About Me</h1><span>&nbsp;
        {{ text }}</span>
    <div class="p-1">
      <h2>Yoon Hwan Cho</h2>
    </div>
    <div class="row p-1">
      <div class="d-grid gap-2 d-md-flex justify-content-md-start">
        <a href="https://drive.google.com/file/d/1pkT456nZ40ewxVq11ezU6v4pJgmSFBD9/view?usp=share_link" target="_blank"><button type="button" class="btn btn-info mb-2 white">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-journal-code" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M8.646 5.646a.5.5 0 0 1 .708 0l2 2a.5.5 0 0 1 0 .708l-2 2a.5.5 0 0 1-.708-.708L10.293 8 8.646 6.354a.5.5 0 0 1 0-.708zm-1.292 0a.5.5 0 0 0-.708 0l-2 2a.5.5 0 0 0 0 .708l2 2a.5.5 0 0 0 .708-.708L5.707 8l1.647-1.646a.5.5 0 0 0 0-.708z"/>
            <path d="M3 0h10a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2v-1h1v1a1 1 0 0 0 1 1h10a1 1 0 0 0 1-1V2a1 1 0 0 0-1-1H3a1 1 0 0 0-1 1v1H1V2a2 2 0 0 1 2-2z"/>
            <path d="M1 5v-.5a.5.5 0 0 1 1 0V5h.5a.5.5 0 0 1 0 1h-2a.5.5 0 0 1 0-1H1zm0 3v-.5a.5.5 0 0 1 1 0V8h.5a.5.5 0 0 1 0 1h-2a.5.5 0 0 1 0-1H1zm0 3v-.5a.5.5 0 0 1 1 0v.5h.5a.5.5 0 0 1 0 1h-2a.5.5 0 0 1 0-1H1z"/>
          </svg> Resume
        </button></a>

        <a href="https://www.linkedin.com/in/yoonhcho/" target="_blank"><button type="button" class="btn btn-success mb-2 hover-black">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-linkedin" viewBox="0 0 16 16">
            <path d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1.146H1.175C.526 16 0 15.487 0 14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248-.015-.709-.52-1.248-1.342-1.248-.822 0-1.359.54-1.359 1.248 0 .694.521 1.248 1.327 1.248h.016zm4.908 8.212V9.359c0-.216.016-.432.08-.586.173-.431.568-.878 1.232-.878.869 0 1.216.662 1.216 1.634v3.865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252-1.274 0-1.845.7-2.165 1.193v.025h-.016a5.54 5.54 0 0 1 .016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225h2.4z"/>
          </svg> LinkedIn
        </button></a>
        
        <a href="https://github.com/YoonHCho" target="_blank"><button type="button" class="btn btn-primary mb-2 hover-black">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-github" viewBox="0 0 16 16">
            <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
          </svg> GitHub
        </button></a>
      </div>
      <p>
        I currently live in Southern California and graduated from California State University, Fullerton. I majored in accounting because I liked working with numbers, solving problems to get an answer, and that it will balance if everything was journalized correctly (Asset = Liability + Equity).
      </p>
      <p>
        Recently I enrolled and graduated from an accelerated Web Development Program to pursue a footprint in the Tech industry. I never thought about software engineering as a career because I thought I have to deal with computers and I am not tech savvy, but after challenging myself to finish the program, I realized working with code was more fun than I realized, constantly solving problems.
      </p>

      <p>
        My education in accounting has provided me with a strong foundation in analytical thinking, attention to detail, and problem-solving. My coding BootCamp experience has given me practical experience in HTML, CSS, JavaScript, React, Node.js, Express.js, and using the relational database PostgreSQL. I am ready to use my newfound skills in practice in the real-world work environment and also continue to learn new technologies.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['theme', 'textColor'],
  name: 'About',
  data() {
    return {
      typing: ["I am a Software Engineer. ", "I used to work with numbers. ", "Now I work with code. "],
      loopElement: 0,
      text: ' ',
      isDeleting: false,
      time: 150,
    }
  },
  methods: {
    typewrite() {
      const i = this.loopElement % this.typing.length;
      const fullText = this.typing[i];
      const updateText = !this.isDeleting ? fullText.substring(0, this.text.length + 1) : fullText.substring(0, this.text.length - 1);
      this.text = updateText;

      if (!this.isDeleting && updateText === this.typing[i]) {
        this.isDeleting = true;
        this.time = 50;
      } else if (this.isDeleting && updateText === '') {
        this.isDeleting = false;
        this.loopElement++;
        this.time = 150;
      }
    }
  },
  mounted() {
    let startTypewrite = setInterval(() => {
      this.typewrite();
    }, this.time);

    return () => {
      clearInterval(startTypewrite);
    }
  }
}
</script>

<style scoped>
.about-container {
  width: 65%;
  border-radius: 10px;
}

.same-line {
  display: inline-block;
}

.white {
  color: white;
}

.hover-black:hover {
  color: black;
}

@media only screen and (min-width: 300px) {
  img {
    max-width: 250px;
  }
}
@media only screen and (max-width: 992px) {
    .about-container {
      width: 90%;
    }
  }
</style>