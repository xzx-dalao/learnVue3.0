<template>
  <div class="container">
    <header class="header">
      <slot name="header"></slot>
    </header>
    <main class="main">
      <slot></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>


<script>
export default {
  name: "",
  setup() {},
};
</script>
<style scoped>
/* @import url(); 引入css类 */
.container .header {
  font-size: 8px;
  color: red;
}
.container .main {
  margin-left: 15px;
}

</style>