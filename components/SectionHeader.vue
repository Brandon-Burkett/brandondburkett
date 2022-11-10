.<template>
  <div class="section-header">
    <img
      :src="icon"
      :alt="alt"
    >
    <h2>{{ title }}</h2>
  </div>
</template>

<script setup>
const props = defineProps(["icon", "alt", "title"]);
</script>

<style scoped lang="scss">
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
</style>