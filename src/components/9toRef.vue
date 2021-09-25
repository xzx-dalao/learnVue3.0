<template>
<div>
<p>{{state}}</p>
<button @click="myfun">++</button>
</div>
</template>

<script>
//ref修改数据不会影响原来数据，会触发更新
//toRef修改数据会影响原来数据，不会触发更新
import {ref,toRef} from 'vue'
export default {
name:'', 
setup(){
    let obj={name:'xzx'}
    let state=ref(obj.name)
    let state2=toRef(obj,'name')
    function myfun(){
        
        state.value='eee'
        console.log(obj)
        console.log(state)
        // state2.value='zs'
        //   console.log(obj)
        // console.log(state)
    }
    return {state,myfun}
}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>