<template>
  <section>
    <div class="main-container">
      <div class="hero-main">
        <div class="hero-intro">
          <h3>Hello there! My name is</h3>
        </div>
        <div class="hero-name">
          <h1>Brandon Burkett</h1>
        </div>
        <div class="hero-tagline">
          <h2>I solve problems.</h2>
        </div>
        <div class="hero-description">
          <p>I’m a senior Computer Science & Engineering student at Bucknell University. I’m passionate about building software that makes a difference.</p>
          <p>I'm currently looking for full-time positions after my graduation in spring of 2023.</p>
        </div>
        <div class="hero-links">
          <!-- <a
            href="/resume.pdf"
            class="hero-link button-outline"
            target="_blank"
          ><img
              src="@/assets/icons/file.svg"
              alt=""
            >resume</a> -->
          <a
            href="/resume.pdf"
            class="hero-link button-fill"
            target="_blank"
          ><img
              src="@/assets/icons/file.svg"
              alt="file icon"
            >View Resume</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
</script>

<style scoped lang="scss">
.hero-main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 100vh;
  padding-inline: 0;
}
.hero-intro {
  margin-bottom: 1em;
  line-height: 1;
}
.hero-name {
  font-weight: bold;
  line-height: 1;

  margin-bottom: 0.5em;
}
.hero-tagline {
  font-weight: bold;
  line-height: 1;
  color: var(--primary-text-color-light);
  margin-bottom: 1em;
}
.hero-description {
  max-width: 75ch;
  p {
    margin-top: 1em;
  }
}
.hero-links {
  display: flex;
  margin-top: 2em;
  align-items: center;
  font-size: 1.1em;
  img {
    float: left;
    margin-right: 0.5em;
    width: 1.3em;
    height: 1.3em;
  }
  // .button-fill img {
  //   filter: var(--white-svg-color-filter);
  // }
  // .button-outline img {
  //   filter: var(--primary-svg-color-filter);
  // }
  // .button-outline:hover img {
  //   filter: var(--accent-svg-color-filter);
  // }
}

.hero-link {
  margin-right: 1em;
}
</style>