<template>
    <div name="show-shopping">
        <ul class="goodList">
            <li v-for="item in list" :key="item.img">
                <img v-bind:src="item.img" alt="">
                <p>{{item.goodName}}</p>
            </li>
        </ul>
    </div>
</template>

<style>
.goodList li{
    width: 180px;
    height: 200px;
    list-style: none;
    float: left;
    font-size: 9px;
    color: red;
}
.goodList img{
    width: 165px;
    height: 160px;
}
</style>

<script>
export default {
    name:'show-shopping',
    data(){
        var _this = this;
        var url = '';
        if(_this.id == 1){
            url = 'json/sj.json';     
        }else if(_this.id == 2){
            url = 'json/bjb.json';
        }else{
            url = 'json/sj.json';
        }
        this.$http.get(url).then(function(res){
            _this.list = res.data;
        })
        return {
            list : []
        }
    },
    props :{
        id : Number
    },
    watch:{
        id(){
            var _this = this;
            var url = '';
            if(_this.id == 1){
               url = 'json/sj.json';     
            }else if(_this.id == 2){
                url = 'json/bjb.json';
            }else{
                url = 'json/sj.json';
            }
            this.$http.get(url).then(function(res){
                console.log(res.data)
                _this.list = res.data;
            })
            return {
                list : []
            }            
        }
    }   
}
</script>

