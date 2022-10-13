<template>
  <div class="sections">
    <SectionItem
      :items="userItems"
      :header_items="headerUserItems"
      :number="6"
      :color="'aqua'"
    />
    <SectionItem
      :items="selectedItems"
      :header_items="headerSelectedItems"
      :number="1"
      :color="'coral'"
    />
  </div>
</template>

<script>
import SectionItem from "./SectionItem.vue";
import { mapGetters } from "vuex";
export default {
  components: {
    SectionItem,
  },
  computed: {
    ...mapGetters([
      "userItems",
      "selectedItems",
      "headerUserItems",
      "headerSelectedItems",
    ]),
  },
};
</script>