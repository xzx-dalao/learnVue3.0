<template>
<div>
<p ref="box">我我我我我我</p>

</div>
</template>

<script>
import {ref} from 'vue'
import { onMounted, onUpdated, onUnmounted } from 'vue'
export default {
name:'', 
setup(){
let box=ref(null)
   onMounted(() => {
      console.log('mounted!',box.value)
    })
    onUpdated(() => {
      console.log('updated!',box.value)
    })
    onUnmounted(() => {
      console.log('unmounted!',box.value)
    })
 
    return {box}
}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>