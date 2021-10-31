<template>
    <div name="show">
        <ul class="goodList">
            <li v-for="good in list">
                <img v-bind:src="good.img">
                <p>{{good.goodName}}</p>
            </li>
        </ul>

    </div>
</template>
<style>
    .goodList li {
        width: 200px;
        height: 200px;
        list-style: none;
        float: left;
        font-size: 9px;
        color: red;
        margin-bottom: 50px;
    }

    .goodList img {
        width: 180px;
        height: 180px;
    }
</style>
<script>
    export default {
        props: {
            goodId: {
                type: Number,
                defaultValue: 1
            }
        },
        name: "show",
        data() {
            var obj = this;
            var url = "";
            if (obj.goodId === 1 || obj.goodId === 0) {
                url = "json/bjb.json";
            } else if (obj.goodId === 2) {
                url = "json/shouji.json";
            }
            this.$http.get(url).then((res) => {
                console.log(res);
                obj.list = res.data;
            });
            return {
                list: []
            };
        },
        watch: {
            goodId() {
                var obj = this;
                var url = "";
                if (obj.goodId === 1 || obj.goodId === 0) {
                    url = "json/bjb.json";
                } else if (obj.goodId === 2) {
                    url = "json/shouji.json";
                }
                this.$http.get(url).then((res) => {
                    console.log(res);
                    obj.list = res.data;
                });
            }
        }
    }
</script>