<template>
  <div>
    <slot1>
      <template v-slot:header>
        <h1>Here might be a page title</h1>
      </template>

      <template v-slot:default>
        <img src="../assets/imge/1.jpg" alt="" width="75" height="75">
      </template>

      <template v-slot:footer>
        <p>Here's some contact info</p>
      </template>
    </slot1>
  </div>
</template>

<script>

import slot1 from "./15slotchlid.vue";
export default {
  name: "vuee",
  data() {
    return {};
  },
  components: { slot1 },
  //生命周期 - 创建完成（访问当前this实例）
  created() {},
  //生命周期 - 挂载完成（访问DOM元素）
  mounted() {},
  methods: {},
};
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>