<template>
  <footer class="footer is-fixed-bottom">
    <div class="content has-text-centered">
      <p>
        <strong class="glitchy" data-text="{Izzy .}">{Izzy .}</strong> was made with
        <span style="color: #000;">&hearts;</span> by
        <a
          href="https://www.linkedin.com/in/izzyahmad/"
          style="color:#000; text-decoration: underline;"
        >Izzy Ahmad</a>.
        <br>
        <a href="https://bulma.io">
          <img
            src="~/assets/img/made-with-bulma--black.png"
            alt="Made with Bulma"
            width="128"
            height="24"
          >
        </a>
      </p>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style>
.footer{
      padding: 1.5rem 0;
}

.glitchy {
  white-space: nowrap;
  position: relative;
  display: inline-block;
  margin: 0;
  padding: 0;
  font-size: 1rem;
}

.glitchy::before,
.glitchy::after {
  content: attr(data-text);
  position: absolute;
  left: 0;
  top: 0;
  color: inherit;
  background-color: inherit;
  overflow: hidden;
}

.glitchy::before {
  left: 1px;
  text-shadow: -1px 0 #ffc0cb;
  -o-clip-path: inset(100% 0 0% 0);
  -ms-clip-path: inset(100% 0 0% 0);
  -moz-clip-path: inset(100% 0 0% 0);
  -webkit-clip-path: inset(100% 0 0% 0);
  clip-path: inset(100% 0 0% 0);
  animation: glitch-anim-2 1s infinite linear alternate-reverse;
}

.glitchy::after {
  left: -1px;
  text-shadow: -1px 0 rgba(0, 255, 255, 0.4);
  -o-clip-path: inset(100% 0 0% 0);
  -ms-clip-path: inset(100% 0 0% 0);
  -moz-clip-path: inset(100% 0 0% 0);
  -webkit-clip-path: inset(100% 0 0% 0);
  clip-path: inset(100% 0 0% 0);
  animation: glitch-anim 0.7s infinite linear alternate-reverse;
}
</style>
