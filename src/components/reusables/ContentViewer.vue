<template>
  <div class="ContentViewer">
    <h4>{{ title }}</h4>
    <div class="content">
      <div v-if="contentType == 'verse'" class="text_content">
        <div class="verse">
          <p class="reference">James 1:1</p>
          <p class="refreference_text">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nam,
            voluptates.
          </p>
        </div>
      </div>
      <div class="slide_content" v-if="contentType == 'slide'"></div>
      <div class="song_content" v-if="contentType == 'song'">
        <p class="stanza">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Accusamus,
          iusto!
        </p>
        <p class="stanza">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Accusamus,
          iusto!
        </p>
        <p class="stanza">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Accusamus,
          iusto!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      default: "Content",
      type: String,
    },
    content: {
      type: Array,
    },
    contentType: {
      type: String,
    },
  },
};
</script>

<style lang="scss">
.ContentViewer {
  h4 {
    text-align: center;
  }
  border-radius: 10px;
  background: var(--secondaryColor);
  width: 100%;
  padding: 10px;
}
</style>