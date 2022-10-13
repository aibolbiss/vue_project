<template>
  <div class="headers">
    <HeaderItem :items="headerUserItems" />
    <HeaderItem :items="headerSelectedItems" :center="true" />
  </div>
</template>

<script>
import HeaderItem from "./HeaderItem.vue";
import { mapGetters } from "vuex";
export default {
  components: {
    HeaderItem,
  },
  computed: {
    ...mapGetters(["headerUserItems", "headerSelectedItems"]),
  },
};
</script>