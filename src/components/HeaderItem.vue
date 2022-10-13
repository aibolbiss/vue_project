<template>
  <div
    class="header"
    :style="{ justifyContent: center ? 'center' : 'space-between' }"
  >
    <ul v-for="item in items" :key="item.id" class="header_item">
      <li>{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
    },
    center: {
      type: Boolean,
    },
  },
};
</script>