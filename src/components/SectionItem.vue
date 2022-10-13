<template>
  <div class="section">
    <ul
      v-for="(item, idx) in items"
      :key="item.id"
      class="section_item"
      :class="color === 'aqua' ? 'aqua' : 'coral'"
    >
      <li @click="addItem(idx)">{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
    },
    header_items: {
      type: Array,
    },
    number: {
      type: Number,
    },
    color: {
      type: String,
    },
  },
  methods: {
    addItem(idx) {
      if (this.header_items.length < this.number) {
        this.header_items.push(this.items[idx]);
        this.items.splice(idx, 1);
      }
    },
  },
};
</script>

<style>
.aqua:hover {
  background-color: aqua;
}
.coral:hover {
  background-color: coral;
}
</style>