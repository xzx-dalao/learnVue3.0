<template>
<div>app2:{{testMsg}}</div>
</template>

<script>
import { inject } from 'vue'
export default {
name:'', 
setup(){
const testMsg = inject("msg")   
return {testMsg}

}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>