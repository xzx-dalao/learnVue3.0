<template>
  <div>
    <div>
      <div class="one">
        <img
          src="./index1.jpg"
          ref="btn"
          @mouseover="mouseover"
          @mouseout="mouseout"
          width="350"
          height="220"
        />
      </div>
      <div
        id="mohu"
        v-show="isshow"
        @mouseover="mouseover"
        @mouseout="mouseout"
      ></div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "",
  setup() {
    let isshow = ref(false);
    const btn = ref(null);
    function mouseover() {
      btn.value.width = 400;
      btn.value.height = 250;
      isshow.value = true;
    }
    function mouseout() {
    btn.value.width = 400;
      btn.value.height = 250;
      isshow.value = false;
    }
    return { isshow, mouseover, mouseout, btn };
  },
  // data() {
  //   return {
  //     isshow: false,
  //   };
  // },
  // methods: {
  //   mouseover() {
  //     this.$refs.btn.style.height = 250 + "px";
  //     this.$refs.btn.style.width = 400 + "px";
  //     this.isshow = true;
  //   },
  //   mouseout() {
  //     this.$refs.btn.style.height = 220 + "px";
  //     this.$refs.btn.style.width = 350 + "px";
  //     this.isshow = false;
  //   },
  // },
};
</script>
<style scoped>
/* @import url(); 引入css类 */
.one {
  width: 350px;
  height: 280px;
  /* border: 1px solid black; */
  overflow: hidden;
  margin-left: 250px;
  margin-top: 250px;
}

img {
  transition: all 1s;
}

#mohu {
  transition: all 5s;
  background-color: red;
  opacity: 0.2;
  position: relative;
  margin-top: -280px;
  margin-left: 250px;
  width: 350px;
  height: 220px;
}
</style>