<script setup>
useHead({
  titleTemplate(titleChunk) {
    return titleChunk ? `${titleChunk} - Brandon Burkett` : "Brandon Burkett";
  },
  viewport: "width=device-width, initial-scale=1, maximum-scale=1",
  charset: "utf-8",
  meta: [
    {
      name: "description",
      content:
        "I'm a senior Computer Science & Engineering student at Bucknell University.",
    },
    {
      name: "author",
      content: "Brandon Burkett",
    },
  ],
  link: [{ rel: "icon", type: "image/x-icon", href: "/favicon.ico" }],
});
</script>

<template>
  <div>
    <NuxtPage />
  </div>
</template>

<style lang="scss">
/* ----- RESET (https://piccalil.li/blog/a-modern-css-reset/) ----- */

/* Box sizing rules */
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* Remove default margin */
body,
h1,
h2,
h3,
h4,
p,
figure,
blockquote,
dl,
dd {
  margin: 0;
}

/* Remove list styles on ul, ol elements with a list role, which suggests default styling will be removed */
ul[role="list"],
ol[role="list"] {
  list-style: none;
}

/* Set core root defaults */
html:focus-within {
  scroll-behavior: smooth;
}

/* Set core body defaults */
body {
  min-height: 100vh;
  text-rendering: optimizeSpeed;
  line-height: 1.5;
}

/* A elements that don't have a class get default styles */
a:not([class]) {
  text-decoration-skip-ink: auto;
}

/* Make images easier to work with */
img,
picture {
  max-width: 100%;
  display: block;
}

/* Inherit fonts for inputs and buttons */
input,
button,
textarea,
select {
  font: inherit;
}

/* Remove all animations, transitions and smooth scroll for people that prefer not to see them */
@media (prefers-reduced-motion: reduce) {
  html:focus-within {
    scroll-behavior: auto;
  }

  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}

/* ----- TYPOGRAPHY ----- */

:root {
  --primary-text-color: rgb(0, 56, 101);
  --primary-text-color-light: rgb(0, 56, 101, 0.55);
  --primary-bg-color: rgb(251, 251, 251);
  --accent-text-color: rgb(255, 20, 147);
  --accent-text-color-dark: rgb(255, 20, 147, 0.8);
  --accent-text-color-light: rgb(255, 20, 147, 0.3);
  --accent-text-color-lightest: rgb(255, 20, 147, 0.05);
  --primary-svg-color-filter: invert(7%) sepia(87%) saturate(6039%)
    hue-rotate(195deg) brightness(103%) contrast(103%);
  --accent-svg-color-filter: invert(37%) sepia(85%) saturate(7475%)
    hue-rotate(316deg) brightness(103%) contrast(101%);
  --white-svg-color-filter: invert(100%) sepia(0%) saturate(0%)
    hue-rotate(332deg) brightness(103%) contrast(105%);
}

/* Set the default font family */
html {
  font-family: "Roboto", sans-serif;
  color: var(--primary-text-color);
  background-color: var(--primary-bg-color);
}
h1 {
  font-size: clamp(2rem, 3vw + 0.5rem, 4rem);
}
h2 {
  font-size: clamp(2rem, 2vw + 0.5rem, 3.5rem);
}
h3 {
  font-size: clamp(1.6rem, 1.5vw + 0.5rem, 2rem);
  font-weight: normal;
}
h4 {
  font-size: clamp(1rem, 0.8vw + 0.5rem, 1.2rem);
  font-weight: normal;
}
p {
  font-size: clamp(1rem, 1vw + 0.5rem, 1.2rem);
}

/* ----- GLOBAL ----- */

html {
  scroll-behavior: smooth;
}
.main-container {
  // padding: 0 1rem;
  // margin: 0 1.5rem;
}

.button-fill,
.button-outline {
  cursor: pointer;
  position: relative;
  padding: 0.5rem 1.5rem;
  border-radius: 0.25em;
  box-shadow: rgba(0, 0, 0, 0.35) 1px 1px 3px;
  border: 2px solid var(--accent-text-color);
  transition: all 0.2s ease-in-out;
}

.button-fill::after,
.button-outline::after {
  content: "";
  border-radius: 0.25em;
  position: absolute;
  z-index: -1;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  box-shadow: inset 0 0 0.2rem var(--accent-text-color),
    0 0 0.7rem var(--accent-text-color);
  opacity: 0;
  transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
}

.button-fill {
  background-color: var(--accent-text-color);
  color: var(--primary-bg-color);
}
.button-fill:hover,
.button-fill:focus {
  background-color: var(--accent-text-color-dark);
}

.button-outline {
  color: var(--primary-text-color);
}
.button-outline:hover,
.button-outline:focus {
  background-color: var(--accent-text-color-lightest);
}

.button-fill:hover::after,
.button-outline:hover::after {
  opacity: 1;
}
.main-container {
  // padding: 0 clamp(1rem, 2vw, 2rem);
  // width: clamp(20rem, 55vw, 50rem);
  padding: 0 1rem;
  // width: clamp(18rem, 20rem + 10vw, 50rem);
  margin: 0 auto;
}

/* Extra small devices (phones, 400px and down) */
@media only screen and (max-width: 400px) {
  .main-container {
    width: 100%;
  }
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (min-width: 400px) {
  .main-container {
    width: clamp(20rem, 14rem + 40vw, 50rem);
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .main-container {
    width: clamp(18rem, 14rem + 40vw, 50rem);
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .main-container {
    width: clamp(18rem, 16rem + 40vw, 50rem);
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .main-container {
    width: clamp(18rem, 18rem + 40vw, 50rem);
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .main-container {
    width: clamp(18rem, 20rem + 40vw, 50rem);
  }
}
// section {
//   display: flex;
//   flex-direction: column;
//   align-items: center;
//   justify-content: center;
// }

// @media screen and (min-width: 25rem) and (max-width: 30rem) {
//   .main-container {
//     // margin: 0 1.5rem;

//   }
// }

// @media screen and (min-width: 30rem) and (max-width: 40rem) {
//   body {
//     // font-size: 1.1rem;
//   }
//   .main-container {
//     // margin: 0 15vw;
//   }
// }
// @media screen and (min-width: 40rem) and (max-width: 50rem) {
//   body {
//     // font-size: 1.2rem;
//   }
//   .main-container {
//     // margin: 0 17.5vw;
//   }
// }
// @media screen and (min-width: 50rem) and (max-width: 60rem) {
//   body {
//     // font-size: 1.4rem;
//   }
//   .main-container {
//     // margin: 0 20vw;
//   }
// }
// @media screen and (min-width: 60rem) {
//   body {
//     // font-size: 1.5rem;
//   }
//   .main-container {
//     // margin: 0 22.5vw;
//     max-width: 50rem;
//   }
// }
</style>