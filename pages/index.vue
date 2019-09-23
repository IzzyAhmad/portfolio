<template>
  <div>
    <section class="section index-section">
      <div class="container">
        <div class="columns is-desktop">
          <div class="column is-full">
            <p class="has-text-centered typing-container">
              I am
              <span class="typing"></span>
            </p>
          </div>
        </div>
        <div class="columns is-desktop">
          <div class="column is-full has-text-centered">
            <a class="button is-white is-medium button-link" href="https://github.com/IzzyAhmad">
              <span class="icon">
                <i class="fab fa-github-alt"></i>
              </span>
              <span>GitHub</span>
            </a>
            <a
              class="button is-white is-medium button-link"
              href="https://stackoverflow.com/users/5633231/izzy-ahmad"
            >
              <span class="icon">
                <i class="fab fa-stack-overflow"></i>
              </span>
              <span>Stack Overflow</span>
            </a>
            <a
              class="button is-white is-medium button-link"
              href="https://www.linkedin.com/in/izzyahmad/"
            >
              <span class="icon">
                <i class="fab fa-linkedin-in"></i>
              </span>
              <span>LinkedIn</span>
            </a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Typed from "typed.js";

export default {
  mounted() {
    var typed = new Typed(".typing", {
      strings: [
        "<strong>Application Engineer</strong>.",
        "<strong>Front-end Developer</strong>.",
        "<strong>Hackathon Enthusiast</strong>."
      ],
      typeSpeed: 80,
      backSpeed: 50,
      backDelay: 2000,
      loop: true
    });
  },
  // asyncData() {
  //   // simulate loading for 5 seconds
  //   return new Promise((resolve) => {
  //     setTimeout(function () {
  //       resolve({})
  //     }, 5000)
  //   })
  // }
};
</script>

<style>
.index-section {
  /* border: 2px solid red; */
  height: 100vh;
}

/* .container{
    border: 2px solid red;
} */
.typing-container {
  margin-top: 30vh;
  font-size: 4em;
}

.button-link {
  margin: 1em;
}

/* mobile */
@media (min-width: 320px) and (max-width: 480px) {
  .typing-container {
    margin-top: 30vh;
    font-size: 1.5em;
  }

  .button-link {
    margin: 0.1em;
  }
}

/* tablet */
@media (min-width: 768px) and (max-width: 1024px) {
  .typing-container {
    margin-top: 35vh;
    font-size: 3.5em;
  }
}
</style>
