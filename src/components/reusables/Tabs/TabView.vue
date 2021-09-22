<template>
  <div class="TabsView">
    <div class="tab_switcher">
      <button
        v-for="tab in tabs"
        :key="tab.title"
        :class="{ active_tab: tab.isActive }"
        @click="selectTab(tab)"
      >
        {{ tab.title }}
      </button>
    </div>

    <div class="tabs_details">
      <!-- <transition-group enter-active-class="animate__slideInUp"> -->
      <slot></slot>
      <!-- </transition-group> -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedTabIndex: 0,
      tabs: [],
    };
  },
  methods: {
    selectTab(selectedTab) {
      this.tabs.forEach((tab) => {
        tab.isActive = tab.title == selectedTab.title;
      });
    },
  },
  created() {
    this.tabs = this.$children;
  },
};
</script>

<style lang="scss">
.TabsView {
  width: 100%;
  height: 100%;
  .tab_switcher {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 5px;
    padding: 8px;
    button {
      font-size: var(--textNormal);
    }
    .active_tab {
      background: var(--activeColor);
    }
  }
  .tabs_details {
    padding: 10px;
    height: 100%;
  }
  .views_wrapper {
    width: 100%;
  }
}
</style>