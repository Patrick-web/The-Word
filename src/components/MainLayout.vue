<template>
  <div class="main_layout">
    <section class="top_section">
      <pinned-history />
      <preview />
      <live />
    </section>
    <section class="bottom_section"></section>
  </div>
</template>

<script>
import Live from "./panels/Live.vue";
import PinnedHistory from "./panels/Pinned-History.vue";
import Preview from "./panels/Preview.vue";
export default {
  components: { PinnedHistory, Preview, Live },
};
</script>

<style lang="scss">
.main_layout {
  height: 100%;
  section {
    resize: vertical;
    border-radius: 10px;
  }
  .top_section {
    height: 48%;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    padding: 10px;
    margin-bottom: 10px;
  }
  .bottom_section {
    height: 50%;
  }
}
</style>