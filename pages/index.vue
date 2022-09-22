<script>
import TheShowcase from "~~/components/TheShowcase.vue";
</script>

<template>
  <div class="root">
    <header>
      <TheHeader />
    </header>

    <main>
      <TheHero />

      <TheAbout />

      <TheShowcase />

      <TheContact />

      <TheSocialIcons />
    </main>

    <footer>
      <TheFooter />
    </footer>
  </div>
</template>


<style lang="scss">
header {
  display: flex;
  position: fixed;
  top: 0px;
  z-index: 1;
  width: 100%;
}
a {
  color: var(--primary-text-color);
  text-decoration: none;
}
ul {
  list-style: none;
}
.scroll-lock {
  overflow: hidden;
}
</style>