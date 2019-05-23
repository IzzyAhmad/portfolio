<template>
  <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <a class="navbar-item title-logo" href="#" data-text="{Izzy .}">{Izzy .}</a>

      <!-- <a
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarMenu"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>-->
    </div>

    <div class="navbar-menu" id="navbarMenu">
      <div class="navbar-end">
        <!-- <a class="navbar-item">Home</a>
        <a class="navbar-item">Experience</a>
        <a class="navbar-item">Language</a>
        <a class="navbar-item">Contact</a>-->
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  mounted() {
    // Get all "navbar-burger" elements
    const $navbarBurgers = Array.prototype.slice.call(
      document.querySelectorAll(".navbar-burger"),
      0
    );

    // Check if there are any navbar burgers
    if ($navbarBurgers.length > 0) {
      // Add a click event on each of them
      $navbarBurgers.forEach(el => {
        el.addEventListener("click", () => {
          // Get the target from the "data-target" attribute
          const target = el.dataset.target;
          const $target = document.getElementById(target);

          // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
          el.classList.toggle("is-active");
          $target.classList.toggle("is-active");
        });
      });
    }
  }
};
</script>

<style>
.title-logo {
  font-size: 3em;
  font-weight: bold;
  padding-left: 2em;
}

.title-logo::before,
.title-logo::after {
  content: attr(data-text);
  position: absolute;
  padding-left: 2em;
  color: inherit;
  background-color: inherit;
  overflow: hidden;
}

.title-logo::before {
  left: 2px;
  text-shadow: -1px 0 #ffc0cb;
  -o-clip-path: inset(100% 0 0% 0);
  -ms-clip-path: inset(100% 0 0% 0);
  -moz-clip-path: inset(100% 0 0% 0);
  -webkit-clip-path: inset(100% 0 0% 0);
  clip-path: inset(100% 0 0% 0);
  animation: glitch-anim-2 1s infinite linear alternate-reverse;
}

.title-logo::after {
  left: -2px;
  text-shadow: -1px 0 rgba(0, 255, 255, 0.4);
  -o-clip-path: inset(100% 0 0% 0);
  -ms-clip-path: inset(100% 0 0% 0);
  -moz-clip-path: inset(100% 0 0% 0);
  -webkit-clip-path: inset(100% 0 0% 0);
  clip-path: inset(100% 0 0% 0);
  animation: glitch-anim 0.7s infinite linear alternate-reverse;
}

/* mobile */
@media (min-width: 320px) and (max-width: 480px) {
  .title-logo {
    font-size: 2em;
    padding-left: 0.5em;
  }

  .title-logo::before,
  .title-logo::after {
    content: attr(data-text);
    position: absolute;
    padding-left: 0.5em;
    color: inherit;
    background-color: inherit;
    overflow: hidden;
  }
}

/* tablet */
@media (min-width: 768px) and (max-width: 1024px) {
  .title-logo {
    font-size: 4em;
    padding-left: 1em;
  }

  .title-logo::before,
  .title-logo::after {
    content: attr(data-text);
    position: absolute;
    padding-left: 1em;
    color: inherit;
    background-color: inherit;
    overflow: hidden;
  }
}

@keyframes glitch-anim {
  0% {
    -o-clip-path: inset(100% 0 0% 0);
    -ms-clip-path: inset(100% 0 0% 0);
    -moz-clip-path: inset(100% 0 0% 0);
    -webkit-clip-path: inset(100% 0 0% 0);
    clip-path: inset(100% 0 0% 0);
  }

  50% {
    -o-clip-path: inset(100% 0 0% 0);
    -ms-clip-path: inset(100% 0 0% 0);
    -moz-clip-path: inset(100% 0 0% 0);
    -webkit-clip-path: inset(100% 0 0% 0);
    clip-path: inset(100% 0 0% 0);
  }

  55% {
    -o-clip-path: inset(20% 0 30% 0);
    -ms-clip-path: inset(20% 0 30% 0);
    -moz-clip-path: inset(20% 0 30% 0);
    -webkit-clip-path: inset(20% 0 30% 0);
    clip-path: inset(20% 0 30% 0);
  }

  60% {
    -o-clip-path: inset(19% 0 76% 0);
    -ms-clip-path: inset(19% 0 76% 0);
    -moz-clip-path: inset(19% 0 76% 0);
    -webkit-clip-path: inset(19% 0 76% 0);
    clip-path: inset(19% 0 76% 0);
  }

  65% {
    -o-clip-path: inset(30% 0 20% 0);
    -ms-clip-path: inset(30% 0 20% 0);
    -moz-clip-path: inset(30% 0 20% 0);
    -webkit-clip-path: inset(30% 0 20% 0);
    clip-path: inset(30% 0 20% 0);
  }

  70% {
    -o-clip-path: inset(20% 0 60% 0);
    -ms-clip-path: inset(20% 0 60% 0);
    -moz-clip-path: inset(20% 0 60% 0);
    -webkit-clip-path: inset(20% 0 60% 0);
    clip-path: inset(20% 0 60% 0);
  }

  75% {
    -o-clip-path: inset(0% 0 70% 0);
    -ms-clip-path: inset(0% 0 70% 0);
    -moz-clip-path: inset(0% 0 70% 0);
    -webkit-clip-path: inset(0% 0 70% 0);
    clip-path: inset(0% 0 70% 0);
  }

  80% {
    -o-clip-path: inset(80% 0 0% 0);
    -ms-clip-path: inset(80% 0 0% 0);
    -moz-clip-path: inset(80% 0 0% 0);
    -webkit-clip-path: inset(80% 0 0% 0);
    clip-path: inset(80% 0 0% 0);
  }

  85% {
    -o-clip-path: inset(7% 0 20% 0);
    -ms-clip-path: inset(7% 0 20% 0);
    -moz-clip-path: inset(7% 0 20% 0);
    -webkit-clip-path: inset(7% 0 20% 0);
    clip-path: inset(7% 0 20% 0);
  }

  90% {
    -o-clip-path: inset(20% 0 60% 0);
    -ms-clip-path: inset(20% 0 60% 0);
    -moz-clip-path: inset(20% 0 60% 0);
    -webkit-clip-path: inset(20% 0 60% 0);
    clip-path: inset(20% 0 60% 0);
  }

  95% {
    -o-clip-path: inset(30% 0 20% 0);
    -ms-clip-path: inset(30% 0 20% 0);
    -moz-clip-path: inset(30% 0 20% 0);
    -webkit-clip-path: inset(30% 0 20% 0);
    clip-path: inset(30% 0 20% 0);
  }

  100% {
    -o-clip-path: inset(35% 0 50% 0);
    -ms-clip-path: inset(35% 0 50% 0);
    -moz-clip-path: inset(35% 0 50% 0);
    -webkit-clip-path: inset(35% 0 50% 0);
    clip-path: inset(35% 0 50% 0);
  }
}

@keyframes glitch-anim-2 {
  0% {
    -o-clip-path: inset(100% 0 0% 0);
    -ms-clip-path: inset(100% 0 0% 0);
    -moz-clip-path: inset(100% 0 0% 0);
    -webkit-clip-path: inset(100% 0 0% 0);
    clip-path: inset(100% 0 0% 0);
  }

  50% {
    -o-clip-path: inset(100% 0 0% 0);
    -ms-clip-path: inset(100% 0 0% 0);
    -moz-clip-path: inset(100% 0 0% 0);
    -webkit-clip-path: inset(100% 0 0% 0);
    clip-path: inset(100% 0 0% 0);
  }

  55% {
    -o-clip-path: inset(7% 0 20% 0);
    -ms-clip-path: inset(7% 0 20% 0);
    -moz-clip-path: inset(7% 0 20% 0);
    -webkit-clip-path: inset(7% 0 20% 0);
    clip-path: inset(7% 0 20% 0);
  }

  60% {
    -o-clip-path: inset(50% 0 60% 0);
    -ms-clip-path: inset(50% 0 60% 0);
    -moz-clip-path: inset(50% 0 60% 0);
    -webkit-clip-path: inset(50% 0 60% 0);
    clip-path: inset(50% 0 60% 0);
  }

  65% {
    -o-clip-path: inset(35% 0 50% 0);
    -ms-clip-path: inset(35% 0 50% 0);
    -moz-clip-path: inset(35% 0 50% 0);
    -webkit-clip-path: inset(35% 0 50% 0);
    clip-path: inset(35% 0 50% 0);
  }

  70% {
    -o-clip-path: inset(80% 0 0% 0);
    -ms-clip-path: inset(80% 0 0% 0);
    -moz-clip-path: inset(80% 0 0% 0);
    -webkit-clip-path: inset(80% 0 0% 0);
    clip-path: inset(80% 0 0% 0);
  }

  75% {
    -o-clip-path: inset(5% 0 20% 0);
    -ms-clip-path: inset(5% 0 20% 0);
    -moz-clip-path: inset(5% 0 20% 0);
    -webkit-clip-path: inset(5% 0 20% 0);
    clip-path: inset(5% 0 20% 0);
  }

  80% {
    -o-clip-path: inset(19% 0 60% 0);
    -ms-clip-path: inset(19% 0 60% 0);
    -moz-clip-path: inset(19% 0 60% 0);
    -webkit-clip-path: inset(19% 0 60% 0);
    clip-path: inset(19% 0 60% 0);
  }

  85% {
    -o-clip-path: inset(40% 0 30% 0);
    -ms-clip-path: inset(40% 0 30% 0);
    -moz-clip-path: inset(40% 0 30% 0);
    -webkit-clip-path: inset(40% 0 30% 0);
    clip-path: inset(40% 0 30% 0);
  }

  90% {
    -o-clip-path: inset(19% 0 76% 0);
    -ms-clip-path: inset(19% 0 76% 0);
    -moz-clip-path: inset(19% 0 76% 0);
    -webkit-clip-path: inset(19% 0 76% 0);
    clip-path: inset(19% 0 76% 0);
  }

  95% {
    -o-clip-path: inset(20% 0 60% 0);
    -ms-clip-path: inset(20% 0 60% 0);
    -moz-clip-path: inset(20% 0 60% 0);
    -webkit-clip-path: inset(20% 0 60% 0);
    clip-path: inset(20% 0 60% 0);
  }

  100% {
    -o-clip-path: inset(30% 0 20% 0);
    -ms-clip-path: inset(30% 0 20% 0);
    -moz-clip-path: inset(30% 0 20% 0);
    -webkit-clip-path: inset(30% 0 20% 0);
    clip-path: inset(30% 0 20% 0);
  }
}
</style>
