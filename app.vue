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
    <NuxtWelcome />
  </div>
</template>
