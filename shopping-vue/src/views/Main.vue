<template>
    <div class="main">
        <div class="left">
            <Left></Left>
        </div>
        <div class="right">
        <div class="top">
             <img src="/img/advertising/gg.jpg" alt="">
        </div>
        <div class="bottom">
            <Right></Right>
        </div>

        </div>
    </div>
</template>

<script>
// 组件引用
import Left from '../components/Left.vue'
import Right from '../components/Right.vue'
export default {
    components:{
        Left,
        Right
    }
}
</script>

<style scoped>
*{
    padding: 0px;
    margin: 0px;
}
.left{
    width: 100px;
    float: left;
    margin-right: 20px;
}
.right{
    width: 1000px;
    float: left;
}
.main{
    width: 1200px;
    margin: 20px auto;
}
.top img{
    height: 200px;
    width: 990px;
    margin-top: 3px;
    box-shadow: 1px 5px 5px 5px white;
}
.left, .right{
    background-color: #FFFA10;
}
</style>