<template>
    <div>
        <div class="title">热门推荐</div>
        <ul class="menu">
            <li @click="menu1">手机</li>
            <li @click="menu2">笔记本</li>
            <li>手机</li>
            <li>笔记本</li>
            <li>手机</li>
            <li>笔记本</li>
            <li>手机</li>
            <li>笔记本</li>
            <li>手机</li>
            <li>笔记本</li>
            <li>手机</li>
            <li>笔记本</li>
            <li>手机</li>
            <li>笔记本</li>
        </ul>
    </div>
</template>
<script>
import Msg from './Msg.js';
export default {
    methods:{
        menu1:function(){
            Msg.$emit('val','1')
        },
        menu2:function(){
            Msg.$emit('val','2')
        }
    }
}
</script>
<style scoped>
    *{
        margin: 0px;
        padding: 0px;
        font-size: 15px;
    }
    .title{
        width :100px;
        color :red;
        margin: 5px auto;
    }
    .menu li{
        list-style: none;
        width: 100px;
        height: 30px;
        margin-bottom: 2px;
        background-color: white;
        cursor: pointer;
        line-height: 30px;
    }
</style>
