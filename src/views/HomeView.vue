<template>
  <div id="app">
    <tree-node :node="treeData"></tree-node>
  </div>
</template>

<script>
import TreeNode from "@/components/Tree.vue";

export default {
  components: {
    TreeNode,
  },
  data() {
    return {
      treeData: {
        name: "Root",
        id: 1,
        children: [
          {
            name: "Node 1",
            id: 2,
            children: [
              {
                name: "Node 1.1",
                id: 3,
                children: [],
              },
              {
                name: "Node 1.2",
                id: 4,
                children: [],
              },
            ],
          },
          {
            name: "Node 2",
            id: 5,
            children: [],
          },
        ],
      },
    };
  },
};
</script>
