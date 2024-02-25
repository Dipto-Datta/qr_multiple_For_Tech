<template>
  <div>
    <input
      type="text"
      v-model="inputData"
      placeholder="Enter comma-separated codes"
    />
    <div v-for="code in processedData" :key="code">
      <VueQrcode :value="code" :size="128" :width="200" />
    </div>
  </div>
</template>

<script>
import { ref, watch } from "vue";
import VueQrcode from "vue-qrcode";

export default {
  components: {
    VueQrcode,
  },
  setup() {
    const inputData = ref("");
    const processedData = ref([]);

    watch(inputData, (newValue) => {
      processedData.value = newValue.split(",").map((code) => code.trim());
    });

    return { inputData, processedData };
  },
};
</script>
