<template>
  <div class="social-container">
    <ul class="social-icon-list">
      <li class="social-icon-item"><a
          href="https://github.com/brandon-burkett"
          target="_blank"
          aria-label="GitHub"
        ><img
            src="@/assets/icons/github.svg"
            alt="github icon"
          ></a></li>
      <li class="social-icon-item"><a
          href="https://linkedin.com/brandon-burkett"
          target="_blank"
          aria-label="LinkedIn"
        ><img
            src="@/assets/icons/linkedin.svg"
            alt="linkedin icon"
          ></a></li>
      <li class="social-icon-item"><a
          href="mailto:brandondburkett@gmail.com"
          target="_blank"
          aria-label="email address"
        ><img
            src="@/assets/icons/mail.svg"
            alt="mail icon"
          ></a></li>
    </ul>
  </div>
</template>

<script>
</script>

<style scoped lang="scss">
.social-container {
  padding: 5rem 0rem 0rem;
}
.social-icon-list {
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0.5em 0;
}
.social-icon-item {
  padding: 0 1em 0 1em;
  filter: var(--primary-svg-color-filter);
  &:hover {
    cursor: pointer;
    filter: var(--accent-svg-color-filter);
  }
}
// .social-icon-item:hover {
//   cursor: pointer;
//   filter: var(--accent-svg-color-filter);
// }

// @media screen and (min-width: 768px) {
//   .social-icon-list {
//     position: fixed;
//     flex-direction: column;
//     height: 40%;
//     bottom: 0;
//     left: 4em;
//     margin: 0;
//   }
//   .social-icon-item:last-child {
//     position: relative;
//   }
//   .social-icon-list::after {
//     content: "";
//     position: absolute;
//     top: 100%;
//     height: 10000%;
//     width: 0.25em;
//     left: 50%;
//     margin-left: -0.125em;
//     background-color: var(--primary-text-color);
//   }
//   .social-icon-item {
//     padding: 0 0 1em 0;
//   }
// }
</style>