<template>
  <div>
    <ul>
      <tree-node v-for="node in rootNode" :key="node.id" :node="node">
      </tree-node>
    </ul>
  </div>
</template>

<script>
import TreeNode from "@/components/Tree.vue"; // Import your TreeNode component

export default {
  components: {
    TreeNode,
  },
  data() {
    return {
      rootNode: [
        {
          id: 2,
          name: "Admin",
          children: [
            {
              id: 30,
              name: "Operation",
              children: [
                {
                  id: 35,
                  name: "sufi",
                  children: [], // You can add more levels as needed
                },
                {
                  id: 36,
                  name: "sufi-an",
                  children: [], // You can add more levels as needed
                },
              ],
            },
            {
              id: 30,
              name: "Operation",
              children: [
                {
                  id: 35,
                  name: "sufi",
                  children: [], // You can add more levels as needed
                },
                {
                  id: 36,
                  name: "sufi-an",
                  children: [], // You can add more levels as needed
                },
              ],
            },
          ],
        },
        {
          id: 3,
          name: "Admiin",
          children: [],
        },
      ],
    };
  },
};
</script>
