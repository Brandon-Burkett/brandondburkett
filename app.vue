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
  --accent-text-color-light: rgb(255, 20, 147, 0.3);
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
  padding: 0 1rem;
}

.button-fill {
  a {
    color: var(--primary-text-color);
  }
  cursor: pointer;
  border: 1px solid var(--primary-text-color);
  background-color: var(--accent-text-color);
  color: var(--primary-bg-color);
  padding: 0.5rem 1.5rem;
  border-radius: 2rem;
}
.button-fill:hover,
.button-fill:focus {
  border: 1px solid var(--accent-text-color);
  background-color: var(--primary-text-color);
  transition: background-color 300ms linear;
}

.button-outline {
  a {
    color: var(--primary-text-color);
  }
  cursor: pointer;
  border: 1px solid var(--accent-text-color);
  // background-color: var(--accent-text-color);
  color: var(--primary-text-color);
  padding: 0.5rem 1.5rem;
  border-radius: 2rem;
}
.button-outline:hover,
.button-outline:focus {
  border: 1px solid var(--accent-text-color);
  color: var(--accent-text-color);
  transition: color 300ms linear;
  img {
    filter: var(--accent-svg-color-filter);
    transition: filter 300ms linear;
  }
}

@media screen and (min-width: 25rem) and (max-width: 30rem) {
  .main-container {
    padding: 0 2rem;
  }
}

@media screen and (min-width: 30rem) and (max-width: 40rem) {
  body {
    // font-size: 1.1rem;
  }
  .main-container {
    padding: 0 15vw;
  }
}
@media screen and (min-width: 40rem) and (max-width: 50rem) {
  body {
    // font-size: 1.2rem;
  }
  .main-container {
    padding: 0 17.5vw;
  }
}
@media screen and (min-width: 50rem) and (max-width: 60rem) {
  body {
    // font-size: 1.4rem;
  }
  .main-container {
    padding: 0 20vw;
  }
}
@media screen and (min-width: 40rem) {
  body {
    // font-size: 1.5rem;
  }
  .main-container {
    padding: 0 25%;
  }
}
</style>