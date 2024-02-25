<template>
  <li>
    <span style="cursor: pointer" @click="toggleNode">
      {{ node.name }}
    </span>
    <ul v-if="node.isOpen && hasChildren">
      <tree-node
        v-for="childNode in childNodes"
        :key="childNode.id"
        :node="childNode"
      ></tree-node>
    </ul>
  </li>
</template>

<script>
export default {
  name: "tree-node",
  props: {
    node: Object,
  },
  computed: {
    hasChildren() {
      return this.node.children && this.node.children.length > 0;
    },
    childNodes() {
      return this.node.children || [];
    },
  },
  methods: {
    toggleNode() {
      this.node.isOpen = !this.node.isOpen;
    },
  },
};
</script>
