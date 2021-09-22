<template>
  <div
    v-show="isActive"
    :class="[isActive ? 'animated fadeIn' : 'animated fadeOut']"
  >
    <slot></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  props: {
    selected: { default: false },
    title: {
      required: true,
      type: String,
    },
  },
  mounted() {
    this.isActive = this.selected;
  },
};
</script>

<style>
</style>