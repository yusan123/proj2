<template>
    <div class="main">
        <div class="left">
            <left></left>
        </div>
        <div class="right">
            <div class="top">
                <img src="img/title.jpg">
            </div>
            <div class="bottom">
                <right></right>
            </div>
        </div>
    </div>
</template>
<script>
    import Left from '../components/Left'
    import Right from '../components/Right'
    export default {
        components:{
            Left,
            Right
        }
    }
</script>

<style>
    * {
        padding: 0;
        margin: 0;
    }

    .left {
        width: 100px;
        float: left;
        margin-right: 10px;
    }

    .right {
        width: 1200px;
        float: left;
        margin-left: 10px;
    }
    .main{
        width: 1400px;
        margin: 20px auto;
    }
    .top img{
        height: 300px;
        width: 1200px;
    }
    .left,.right{
        background-color: #f5f5f5;
        height: 500px;
    }
</style>