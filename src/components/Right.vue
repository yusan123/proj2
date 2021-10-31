<template>
    <div>
        <div v-if="kk==1">
            <GoodsList :goodId="1"></GoodsList>
        </div>
        <div v-else-if="kk==2">
            <GoodsList :goodId="2"></GoodsList>
        </div>
        <div v-else>
            <GoodsList :goodId="0"></GoodsList>
        </div>
    </div>
</template>

<script>
    import Msg from './Msg.js'
    import GoodsList from "./GoodsList";

    export default {
        data() {
            return {
                kk: 0
            }
        },
        mounted: function () {
            var _this = this;
            Msg.$on('val', function (m) {
                _this.kk = m;
            })
        },
        components: {
            GoodsList
        }
    }
</script>