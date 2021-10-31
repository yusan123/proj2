<template>
    <div>
        {{kk}}
    </div>
</template>

<script>
    import Msg from './Msg.js'
    export default {
        data(){
            return {
                kk:0
            }
        },
        mounted:function () {
            var _this = this;
            Msg.$on('val',function (m) {
                _this.kk = m;
            })
        }
    }
</script>