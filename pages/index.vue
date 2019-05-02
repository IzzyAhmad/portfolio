<template>
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
    </div>
  </section>
</template>

<script>
import Typed from "typed.js";

export default {
  mounted() {
    var typed = new Typed(".typing", {
      strings: [
        "<strong>Software Developer</strong>.",
        "<strong>Front-end Developer</strong>.",
        "<strong>Hackathon Enthusiast</strong>."
      ],
      typeSpeed: 80,
      backSpeed: 50,
      backDelay: 1000,
      loop: true
    });
  }
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
  margin-top: 40vh;
  font-size: 4em;
}
@media (min-width: 320px) and (max-width: 480px) {
  .typing-container {
    font-size: 2em;
  }
}
</style>
