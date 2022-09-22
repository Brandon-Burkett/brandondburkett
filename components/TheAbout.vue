<template>
  <section id="about">
    <div class="main-container">
      <div class="about-main">
        <div class="section-header">
          <img
            src="@/assets/icons/book.svg"
            alt=""
          >
          <h2>About Me</h2>
        </div>
        <div class="flex">
          <img
            src="@/assets/images/portrait.jpg"
            alt="portrait"
            class="about-portrait"
          >
          <div class="about-text">
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Tempora maiores dolorem eaque, repellat exercitationem voluptas in harum odio tempore fugit laboriosam voluptatem necessitatibus accusamus laudantium autem provident doloribus ipsam repellendus!</p>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Tempora maiores dolorem eaque, repellat exercitationem voluptas in harum odio tempore fugit laboriosam voluptatem necessitatibus accusamus laudantium autem provident doloribus ipsam repellendus!</p>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Tempora maiores dolorem eaque, repellat exercitationem voluptas in harum odio tempore fugit laboriosam voluptatem necessitatibus accusamus laudantium autem provident doloribus ipsam repellendus!</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
</script>

<style scoped lang="scss">
.about-main {
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
.about-portrait {
  width: 100%;
  height: auto;
  max-width: 250px;
  margin: 0 auto;
  margin-bottom: 1rem;
}
.about-text p {
  margin-bottom: 1rem;
}
.flex {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

@media screen and (min-width: 60rem) {
  .about-main {
  }
  .about-text {
    max-width: 60ch;
    padding: 0 2rem 0 0;
  }
  .about-portrait {
    max-width: 350px;
  }
  .flex {
    flex-direction: row-reverse;
    justify-content: space-between;
  }
}
</style>