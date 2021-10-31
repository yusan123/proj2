<template>
    <div>
        <div class="title">热门推荐</div>
        <ul class="menu">
            <li @click="menu1">笔记本电脑</li>
            <li @click="menu2">手机</li>
            <li>服饰</li>
            <li>家电</li>
            <li>笔记本电脑</li>
            <li>笔记本电脑</li>
            <li>笔记本电脑</li>
            <li>笔记本电脑</li>
            <li>笔记本电脑</li>
        </ul>
    </div>
</template>
<script>
    import Msg from './Msg.js'
    export default {
        methods:{
            menu1:function() {
                Msg.$emit("val","11111");
            },
            menu2:function() {
                Msg.$emit("val","22222");
            }
        }
    }
</script>
<style>
    .title {
        width: 100px;
        color: red;
        margin-bottom: 14px;
    }

    .menu li{
        list-style: none;
        height: 50px;
        margin-top: 4px;
        background-color: white;
        line-height: 50px;
    }
</style>