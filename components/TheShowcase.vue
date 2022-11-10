<template>
  <section id="projects">
    <div class="main-container">
      <div class="showcase-main">
        <!-- <div class="section-header">
          <img
            src="@/assets/icons/archive.svg"
            alt=""
          >
          <h2>Projects</h2>
        </div> -->
        <SectionHeader
          :icon="imgSrc"
          title="Projects"
          alt="archive icon"
        />

        <div class="showcase-list">
          <div
            class="showcase-list-item"
            v-for="project in projects"
            :key="project.index"
          >
            <h3 class="showcase-list-item-title">{{ project.title }}</h3>
            <h4 class="showcase-list-item-subtitle">{{ project.subtitle }}</h4>
            <p class="showcase-list-item-description">{{ project.description }}</p>
            <ul class="showcase-list-item-tech">
              <li
                v-for="tech in project.tech"
                :key="tech.index"
              >{{ tech }}</li>
            </ul>
            <div class="showcase-list-item-links">
              <a
                :tabindex="project.links[0].href === '' ? -1 : 0"
                :class="{disabled: !project.links[0].hasOwnProperty('href')}"
                :aria-disabled="!project.links[0].hasOwnProperty('href')"
                :href="project.links[0].href"
                class="showcase-list-item-link left-link"
                target="_blank"
              >
                <img
                  src="@/assets/icons/github.svg"
                  alt="github icon"
                >
                {{ project.links[0].text }}
              </a>
              <a
                :tabindex="project.links[1].href === '' ? -1 : 0"
                :class="{disabled: !project.links[1].hasOwnProperty('href')}"
                :aria-disabled="!project.links[1].hasOwnProperty('href')"
                :href="project.links[1].href"
                class="showcase-list-item-link right-link"
                target="_blank"
              >
                <img
                  src="@/assets/icons/external-link.svg"
                  alt="external link icon"
                >
                {{ project.links[1].text }}
              </a>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { computed } from "vue";
import icon from "../assets/icons/book.svg";

const imgSrc = computed(() => {
  return icon;
});

const projects = ref([
  {
    title: "Personal Website",
    subtitle: "Project Portfolio",
    description:
      "The website you're viewing right now! This is my personal portfolio website to showcase my projects and skills. Designed using Figma, built using Nuxt.js, and deployed using AWS Amplify.",
    tech: ["Nuxt.js", "Vue.js", "HTML", "CSS", "Javascript", "AWS Amplify"],
    links: [
      {
        icon: "github.svg",
        text: "Github",
        href: "https://github.com/Brandon-Burkett/brandondburkett",
        target: "_blank",
      },
      {
        icon: "external-link.svg",
        text: "Check it out!",
        href: "https://www.brandondburkett.com",
        target: "_blank",
      },
    ],
  },
  {
    title: "SpotifyAutoPause",
    subtitle: "Google Chrome Extension",
    description:
      "A Google Chrome extension that pauses Spotify playback when a Chrome tab begins playing audio, and resumes playback when there are no longer any tabs playing audio.",
    tech: ["HTML", "CSS", "Javascript", "Figma"],
    links: [
      {
        icon: "github.svg",
        text: "Github",
        href: "https://github.com/Brandon-Burkett/SpotifyAutoPause",
        target: "_blank",
      },
      {
        icon: "external-link.svg",
        text: "Check it out!",
        href: "https://chrome.google.com/webstore/detail/spotifyautopause/hplodenchomflbmkfnimbnnochgegmej?hl=en-US",
        target: "_blank",
      },
    ],
  },
  {
    title: "Deep Learning Trainer",
    subtitle: "JavaFX Deep Learning Trainer",
    description:
      "A GUI to easily adjust hyperparameters and visualize variations in output between learning models. Implemented using the Deeplearning4J library to train models and display learning rate and accuracy.",
    tech: ["Java", "JavaFX", "Gradle", "Deeplearning4j"],
    links: [
      {
        icon: "github.svg",
        text: "Github",
        target: "_blank",
      },
      {
        icon: "external-link.svg",
        text: "Check it out!",
        target: "_blank",
      },
    ],
  },
  {
    title: "Vaccine Bot",
    subtitle: "Discord Bot",
    description:
      "A Discord bot created during the pandemic to alert users when local vaccination appointments became available. Accomplished using web scraping to get appointment data, and discord.py to alert users",
    tech: ["Python"],
    links: [
      {
        icon: "github.svg",
        text: "Github",
        href: "https://github.com/Brandon-Burkett/VaccineBot",
        target: "_blank",
      },
      {
        icon: "external-link.svg",
        text: "Check it out!",
        target: "_blank",
      },
    ],
  },
  {
    title: "DexMenuApp",
    subtitle: "macOS Menu Bar App",
    description:
      "A macOS app that retrieves and displays Dexcom blood glucose data in the menu bar, allowing users to access blood glucose data directly on their computer for convenience and discretion.",
    tech: ["Python"],
    links: [
      {
        icon: "github.svg",
        text: "Github",
        href: "https://github.com/Brandon-Burkett/dex-menu-app",
        target: "_blank",
      },
      {
        icon: "external-link.svg",
        text: "Check it out!",
        target: "_blank",
      },
    ],
  },
]);
</script>

<style scoped lang="scss">
.showcase-main {
  padding: 1em 0em;
}
// .section-header {
//   margin-bottom: 2em;
//   display: flex;
//   align-items: center;
//   img {
//     float: left;
//     width: 3em;
//     height: 2em;
//     filter: var(--accent-svg-color-filter);
//   }
//   h2 {
//     position: relative;
//     float: right;
//   }
//   h2::after {
//     content: "";
//     position: absolute;
//     bottom: 0em;
//     left: 0;
//     height: 4px;
//     width: 3em;
//     background-color: var(--accent-text-color);
//   }
// }
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
  box-shadow: rgba(0, 0, 0, 0.35) 5px 5px 10px;
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
  &::after {
    content: "";
    position: absolute;
    bottom: -0.3em;
    left: 0;
    height: 2px;
    width: 8em;
    background-color: var(--accent-text-color);
  }
}
// .showcase-list-item-subtitle::after {
//   content: "";
//   position: absolute;
//   bottom: -0.3em;
//   left: 0;
//   height: 2px;
//   width: 8em;
//   background-color: var(--accent-text-color);
// }
.showcase-list-item-tech {
  display: flex;
  padding: 0;
  list-style: none;
  flex-wrap: wrap;
  margin: 1em 0 0 0;
  li {
    margin-top: 0.5em;
    margin-right: 0.5em;
    padding: 0.25em 0.5em;
    background-color: var(--accent-text-color-light);
    box-shadow: rgba(0, 0, 0, 0.35) 1px 1px 3px;
  }
}
// .showcase-list-item-tech li {
//   margin-top: 0.5em;
//   margin-right: 0.5em;
//   padding: 0.25em 0.5em;
//   background-color: var(--accent-text-color-light);
//   box-shadow: rgba(0, 0, 0, 0.35) 1px 1px 3px;
// }
.showcase-list-item-links {
  display: flex;
  margin: 1.5em 0 0 0;
  justify-content: space-around;
  box-sizing: content-box;
  .right-link {
    color: var(--primary-bg-color);
    background-color: var(--primary-text-color);
    img {
      filter: var(--white-svg-color-filter);
    }
  }
  .left-link {
    color: var(--primary-text-color);
    border: 2px solid var(--primary-text-color);
    img {
      filter: var(--primary-svg-color-filter);
    }
  }
}
.showcase-list-item-link {
  display: flex;
  padding: 0.5em 1em;
  align-items: center;
  border-radius: 0.25em;
  box-shadow: rgba(0, 0, 0, 0.35) 2px 2px 4px;
  transition: transform 0.3s, box-shadow 0.3s;
  -webkit-tap-highlight-color: transparent;
  transform: translateZ(0);
  img {
    width: 1.5em;
    height: 1.5em;
    margin-right: 0.5em;
  }
  &:first-child {
    margin-right: 0.5em;
  }
  &:last-child {
    margin-left: 0.5em;
  }
  &.disabled {
    pointer-events: none;
    cursor: default;
    opacity: 0.3;
  }
  &:hover,
  &:focus {
    box-shadow: rgba(0, 0, 0, 0.35) 3px 3px 5px;
    transform: translate(2px, -2px);
  }
}

// .showcase-list-item-link:hover,
// .showcase-list-item-link:focus {
//   box-shadow: rgba(0, 0, 0, 0.35) 3px 3px 5px;
//   transform: translate(2px, -2px);
// }

@media screen and (max-width: 370px) {
  .showcase-list-item-link {
    img {
      width: 1.25em;
      height: 1.25em;
      margin-right: 0.25em;
    }
    line-height: 1em;
    font-size: 1em;
    padding: 2vw 4vw;
  }
}

@media screen and (min-width: 992px) {
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
    .right-link {
      margin-right: 1em;
    }
  }
}
</style>