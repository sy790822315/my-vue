<template>
    <div>
        <div v-if="kk == 1">
            <good-list :id = "1"></good-list>
        </div>
        <div v-else-if="kk == 2">
            <good-list :id = "2"></good-list>
        </div>
        <div v-else>
            <good-list :id = "0"></good-list>
        </div>
    </div>
</template>
<script>
import Msg from './Msg.js'
import GoodList from './GoodList.vue'
export default {
    data(){
        return {
            kk:0
        }
    },
    mounted:function(){
        var _this = this;
        Msg.$on('val',function(e){
            _this.kk = e;
        })
    },
    components:{
        GoodList
    }
}
</script>