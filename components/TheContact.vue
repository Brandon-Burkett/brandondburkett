<template>
  <section id="contact">
    <div class="main-container">
      <div class="contact-main">
        <div class="section-header">
          <img
            src="@/assets/icons/mail.svg"
            alt=""
          >
          <h2>Contact</h2>
        </div>
        <h3 class="contact-title">Get In Touch</h3>
        <p class="contact-text">I'm currently looking for a full-time position. If you're interested, please contact me!</p>
        <div class="contact-links">
          <a
            class="button-outline"
            href="mailto:brandondburkett@gmail.com"
            target="_blank"
          >Say hi!</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
</script>

<style scoped lang="scss">
.contact-main {
  padding: 10vh 0rem;
}
.section-header {
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  img {
    float: left;
    width: 3rem;
    height: 2rem;
    filter: var(--accent-svg-color-filter);
  }
  h2 {
    position: relative;
    float: right;
  }
  h2::after {
    content: "";
    position: absolute;
    bottom: 0.3rem;
    left: 0;
    height: 4px;
    width: 7rem;
    background-color: var(--accent-text-color);
  }
}
.contact-title {
  margin-bottom: 1rem;
  text-align: center;
}
.contact-text {
  margin-bottom: 1rem;
  text-align: center;
}
.contact-links {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>