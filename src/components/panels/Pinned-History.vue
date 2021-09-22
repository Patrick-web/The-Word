<template>
  <div class="PinnedHistory panel">
    <tab-view :tabs="['Pinned', 'History']">
      <tab title="Pinned" key="Pinned" :selected="true">
        Tab One Lorem ipsum dolor sit amet consectetur adipisicing elit.
        Delectus asperiores, consequatur expedita odit facilis aperiam
        consectetur, excepturi odio, voluptate ipsa numquam! Odit ipsa ducimus
        veritatis doloremque quibusdam eum pariatur quis.
      </tab>
      <tab title="History" key="History">
        Tab History Lorem ipsum, dolor sit amet consectetur adipisicing elit.
        Voluptatibus non earum, distinctio facere corporis sequi blanditiis cum
        porro consequatur ducimus fugiat magni quia doloribus, adipisci dolore
        eius ullam ipsa ipsum.
      </tab>
    </tab-view>
  </div>
</template>

<script>
import Tab from "../reusables/Tabs/Tab.vue";
import TabView from "../reusables/Tabs/TabView.vue";
export default {
  components: { TabView, Tab },
};
</script>

<style lang="scss">
.PinnedHistory {
  background: var(--primaryColor);
  height: 100%;
}
</style>