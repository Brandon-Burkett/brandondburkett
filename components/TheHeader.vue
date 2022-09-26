<template>
  <div
    class="header-container"
    :class="{ 'navbar--hidden': !showNavbar }"
  >
    <nav class="primary-nav">
      <a
        href="/"
        class="logo"
      >Brandon Burkett</a>
      <button class="nav-toggle"></button>
      <div
        class="nav-links"
        data-visible="false"
      >
        <ul class="nav-list">
          <li class="nav-list-item"><a href="#about">about</a></li>
          <li class="nav-list-item"><a href="#projects">projects</a></li>
          <li class="nav-list-item"><a href="#contact">contact</a></li>
        </ul>
        <a
          href="/resume.pdf"
          class="nav-resume button-outline"
          target="_blank"
        >resume</a>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
    console.log("mounted");
  },
  methods: {
    handleScroll() {
      const currentScrollPosition =
        window.pageYOffset || document.documentElement.scrollTop;
      if (currentScrollPosition < 0) {
        return;
      }
      // Stop executing this function if the difference between
      // current scroll position and last scroll position is less than some offset
      if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 60) {
        return;
      }
      this.showNavbar = currentScrollPosition < this.lastScrollPosition;
      this.lastScrollPosition = currentScrollPosition;
    },
  },
};
</script>


<script setup>
// var showNavbar = ref(false);
// var lastScrollPosition = ref(0);

// function onScroll() {
//   // Get the current scroll position
//   const currentScrollPosition =
//     window.pageYOffset || document.documentElement.scrollTop;
//   // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
//   if (currentScrollPosition < 0) {
//     return;
//   }
//   // Here we determine whether we need to show or hide the navbar
//   this.showNavbar = currentScrollPosition < this.lastScrollPosition;
//   // Set the current scroll position as the last scroll position
//   this.lastScrollPosition = currentScrollPosition;
// }
onMounted(function () {
  window.addEventListener("click", function () {
    console.log(window.event.target);
    if (window.event.target.classList.contains("nav-toggle")) {
      toggleNav();
    } else if (window.event.target.classList.contains("nav-links")) {
    } else if (
      this.document.querySelector("body").classList.contains("scroll-lock")
    ) {
      toggleNav();
    }
  });
});

function toggleNav() {
  const toggleButton = document.querySelector(".nav-toggle");
  const nav = document.querySelector(".nav-links");
  const body = document.querySelector("body");
  const navVisibility = nav.getAttribute("data-visible");
  if (navVisibility === "false") {
    nav.setAttribute("data-visible", "true");
    toggleButton.setAttribute("aria-expanded", "true");
    body.classList.add("scroll-lock");
  } else {
    nav.setAttribute("data-visible", "false");
    toggleButton.setAttribute("aria-expanded", "false");
    body.classList.remove("scroll-lock");
  }
}
</script>

<style scoped lang="scss">
.header-container {
  position: relative;
  z-index: 3;
  background: var(--primary-bg-color);
  width: 100%;
  padding: 0em 1em;
  transform: translateY(0);
  transition: transform 0.2s ease-out;
}
.primary-nav {
  display: flex;
  min-height: 4rem;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.logo {
  font-size: 1.75rem;
  text-decoration: none;
}
.nav-links {
  display: flex;
  align-items: center;
}
.nav-list {
  display: flex;
  margin: 0;
  padding: 0;
}
.nav-list-item {
}
.nav-list-item a {
  display: inline-block;
  position: relative;
  margin: 0.5em 1em;

  font-size: 1.2rem;
}

/* Fade in */
.nav-list-item a::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0.1em;
  background-color: var(--accent-text-color);
  opacity: 0;
  transition: opacity 300ms, transform 300ms;
}

.nav-list-item a:hover::after,
.nav-list-item a:focus::after {
  opacity: 1;
  transform: translate3d(0, 0.2em, 0);
}
.nav-resume {
  display: inline-block;
  font-size: 1.2rem;
}
.nav-toggle {
  display: none;
  filter: var(--accent-svg-color-filter);
}
.navbar--hidden {
  box-shadow: none;
  transform: translateY(-100%);
}
.button-outline {
  color: var(--primary-text-color);
  padding: 0.25em 1.2em;
  // border: var(--primary-text-color) solid 1px;
}

@media screen and (min-width: 35em) {
  .header-container {
    padding: 0em 3em;
  }
  .nav-resume {
    margin-left: 1em;
  }
}

@media (max-width: 35em) {
  .nav-toggle {
    display: block;
    position: absolute;
    z-index: 9999;
    right: 1rem;
    background: url(@/assets/icons/hamburger.svg) no-repeat;
    background-size: contain;
    width: 2rem;
    height: 2rem;
    border: none;
  }
  .nav-links {
    display: flex;
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    width: 70%;
    min-height: 100vh;
    background: white;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: min(20vh, 10rem) 2em;

    box-shadow: rgba(0, 0, 0, 0.35) 0px 2px 4px;
    transform: translateX(100%);
    transition: transform 0.2s ease-in-out;
    display: none;
  }
  .nav-links[data-visible="true"] {
    transform: translateX(0);
    display: flex;
  }
  .nav-toggle[aria-expanded="true"][aria-expanded="true"] {
    background: url(@/assets/icons/close.svg) no-repeat;
    background-size: contain;
    height: 2rem;
    width: 2rem;
  }
  @supports (backdrop-filter: blur(1rem)) {
    .nav-links {
      background: hsl(0 0% 100% / 0.5);
      backdrop-filter: blur(1rem);
    }
  }
  .nav-list {
    display: flex;
    flex-direction: column;
    padding: 0;
  }
  .nav-resume {
    margin-top: 2em;
  }
}
</style>