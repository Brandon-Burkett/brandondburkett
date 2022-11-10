<template>
  <section id="about">
    <div class="main-container">
      <div class="about-main">
        <!-- <div class="section-header">
          <img
            src="@/assets/icons/book.svg"
            alt=""
          >
          <h2>About Me</h2>
        </div> -->
        <SectionHeader
          icon="../assets/icons/book.svg"
          title="About Me"
          alt="book icon"
        />

        <!-- <div class="flex"> -->
        <!-- <img
            src="@/assets/images/portrait.jpg"
            alt="portrait"
            class="about-portrait"
          > -->
        <div class="about-text">
          <p>In elementary school, teachers often ask children what they wish to be when they grow up. While many kids excitedly claim ‘doctor’, ‘fighter pilot’, or ‘ketchup bottle’, as early as the 4th grade, I knew I wanted to be a computer programmer. Most individuals end up straying from their initial goals of being an astronaut or a vet, but I have always felt a deep sense of passion about building software that makes a difference in peoples lives. </p>

          <p>I am originally from the greater Philadelphia area and am currently a Computer Science and Engineering major at Bucknell University. With my graduation on the horizon in May of 2023, I will be the first member of my family to earn a college degree. </p>

          <p>While on campus, I have helped start a living, learning community called Bed n’ Breakfast for students who share a love of cooking and baking. I have made the engineering building my home and dedicated 5 semesters to being a TA for Data Structures and Algorithms, Software Engineering and Design, and Operating Systems Design. Additionally, I have spent a lot of time at the Hillel House as I’ve participated in multiple semesters of Bucknell’s Jewish Learning Fellowship and I love to explore the Lewisburg area. </p>

          <p>In my free time, I can be found at my computer (duh), eating copious amounts of Chipotle, playing sports with my (not so) little brother, and counting down the days between Apple events. </p>

          <p>While my definition of developing solutions has changed over time from Legos and Lincoln Logs to lines of code, I’ve stayed true to my mission of engineering solutions that improve peoples lives.</p>
        </div>
      </div>
      <!-- </div> -->
    </div>
  </section>
</template>

<script>
</script>

<style scoped lang="scss">
.about-main {
  padding: 10vh 0rem;
}
// .section-header {
//   margin-bottom: 1rem;
//   display: flex;
//   align-items: center;
//   img {
//     float: left;
//     width: 3rem;
//     height: 2rem;
//     filter: var(--accent-svg-color-filter);
//   }
//   h2 {
//     position: relative;
//     float: right;
//   }
//   h2::after {
//     content: "";
//     position: absolute;
//     bottom: 0.3rem;
//     left: 0;
//     height: 4px;
//     width: 7rem;
//     background-color: var(--accent-text-color);
//   }
// }
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
    // max-width: 60ch;
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