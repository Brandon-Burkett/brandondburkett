<template>
  <section id="showcase">
    <div class="main-container">
      <div class="showcase-main">
        <div class="section-header">
          <img
            src="@/assets/icons/archive.svg"
            alt=""
          >
          <h2>Projects</h2>
        </div>

        <div class="showcase-list">
          <div class="showcase-list-item">
            <h3 class="showcase-list-item-title">SpotifyAutoPause</h3>
            <h4 class="showcase-list-item-subtitle">Google Chrome Extension</h4>
            <p class="showcase-list-item-description">A Google Chrome extension that pauses Spotify playback when a Chrome tab begins playing audio, and resumes playback when there are no longer any tabs playing audio.</p>
            <ul class="showcase-list-item-tech">
              <li>HTML</li>
              <li>CSS</li>
              <li>Javascript</li>
              <li>Figma</li>
            </ul>
            <div class="showcase-list-item-links">
              <a
                href="#"
                class="showcase-list-item-link left-link"
                target="_blank"
              >
                <img
                  src="@/assets/icons/github.svg"
                  alt=""
                >
                Github
              </a>
              <a
                href="#"
                class="showcase-list-item-link right-link"
                target="_blank"
              >
                <img
                  src="@/assets/icons/external-link.svg"
                  alt=""
                >
                Check it out!
              </a>
            </div>
          </div>
        </div>

        <div class="showcase-list">
          <div class="showcase-list-item">
            <h3 class="showcase-list-item-title">SpotifyAutoPause</h3>
            <h4 class="showcase-list-item-subtitle">Google Chrome Extension</h4>
            <p class="showcase-list-item-description">A Google Chrome extension that pauses Spotify playback when a Chrome tab begins playing audio, and resumes playback when there are no longer any tabs playing audio.</p>
            <ul class="showcase-list-item-tech">
              <li>HTML</li>
              <li>CSS</li>
              <li>Javascript</li>
              <li>Figma</li>
            </ul>
            <div class="showcase-list-item-links">
              <a
                href="#"
                class="showcase-list-item-link left-link"
                target="_blank"
              >
                <img
                  src="@/assets/icons/github.svg"
                  alt=""
                >
                Github
              </a>
              <a
                href="#"
                class="showcase-list-item-link right-link"
                target="_blank"
              >
                <img
                  src="@/assets/icons/external-link.svg"
                  alt=""
                >
                Check it out!
              </a>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
</script>

<style scoped lang="scss">
.showcase-main {
  padding: 1em 0em;
}
.section-header {
  margin-bottom: 2em;
  display: flex;
  align-items: center;
  img {
    float: left;
    width: 3em;
    height: 2em;
    filter: var(--accent-svg-color-filter);
  }
  h2 {
    position: relative;
    float: right;
  }
  h2::after {
    content: "";
    position: absolute;
    bottom: 0em;
    left: 0;
    height: 4px;
    width: 3em;
    background-color: var(--accent-text-color);
  }
}
.showcase-list {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
.showcase-list-item {
  width: 100%;
  padding: 1.2em;
  background-color: #ffffff;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  border-radius: 0.5em;
  margin-bottom: 3em;
}
.showcase-list-item-title {
  font-weight: bold;
  line-height: 1.2em;
}
.showcase-list-item-subtitle {
  position: relative;
  line-height: 1.2em;
  margin-bottom: 1.5em;
}
.showcase-list-item-subtitle::after {
  content: "";
  position: absolute;
  bottom: -0.3em;
  left: 0;
  height: 2px;
  width: 8em;
  background-color: var(--accent-text-color);
}
.showcase-list-item-tech {
  display: flex;
  padding: 0;
  list-style: none;
  flex-wrap: wrap;
  margin: 1em 0 0 0;
}
.showcase-list-item-tech li {
  margin-top: 0.5em;
  margin-right: 0.5em;
  padding: 0.25em 0.5em;
  background-color: var(--accent-text-color-light);
}
.showcase-list-item-links {
  display: flex;
  margin: 1.5em 0 0 0;
  justify-content: space-evenly;
  .left-link {
    color: var(--primary-bg-color);
    background-color: var(--primary-text-color);
    img {
      filter: var(--white-svg-color-filter);
    }
  }
  .right-link {
    color: var(--primary-text-color);
    border: 2px solid var(--primary-text-color);
    img {
      filter: var(--primary-svg-color-filter);
    }
  }
}
.showcase-list-item-link {
  margin-right: 1em;
  display: flex;
  padding: 0.5em 1em;
  align-items: center;
  border-radius: 0.25em;
  img {
    width: 1.5em;
    height: 1.5em;
    margin-right: 0.5em;
  }
}

@media screen and (min-width: 1650px) {
  .showcase-list-item {
    position: relative;
    // width: 40vw;
    padding: 1.5em;
  }
  .showcase-list-item-links {
    position: absolute;
    top: 0;
    right: 0;
    align-content: flex-start;
    justify-content: flex-end;
    margin: 1.5em 0.5em;
  }
}
</style>