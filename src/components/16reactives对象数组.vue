<template>
  <div>
    <div v-for="item in list[1]" :key="item.id">
      {{ item.id }}--{{ item.name }}
    </div>
  </div>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "",
  setup() {
    let list = reactive([
      [
        { id: 1, name: "李斯" },
        { id: 2, name: "嬴政" },
        { id: 3, name: "赵高" },
        { id: 4, name: "韩非" },
        { id: 5, name: "荀子" },
      ],
      [
        { id: 1, name: "李斯1" },
        { id: 2, name: "嬴政2" },
        { id: 3, name: "赵高3" },
        { id: 4, name: "韩非4" },
        { id: 5, name: "荀子5" },
      ],
    ]);

    return { list };
  },
};
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>