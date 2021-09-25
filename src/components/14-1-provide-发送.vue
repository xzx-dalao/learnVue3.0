<template>
<div>
    app1:
<app2></app2>
</div>
</template>

<script>
import app2 from './App2.vue'
import { provide } from 'vue'


export default {
name:'', 
components:{
    app2
},
setup(){
provide("msg", '透传一段数据')

}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>