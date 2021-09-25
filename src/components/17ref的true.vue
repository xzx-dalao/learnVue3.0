<template>
<div>
    <div v-show="isshow"><p>测试能不能v-show</p></div>
    <button @click="btn">wwwww</button>
</div>
</template>

<script>
import {ref} from 'vue'
export default {
name:'', 
setup(){
let isshow =ref(true)
function btn(){
    isshow.value=!isshow.value
}
return {isshow,btn}
}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>