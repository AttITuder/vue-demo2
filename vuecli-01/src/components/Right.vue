<template>
<div>
    <div v-if="kkk==1">
        <GoodsList :goodsId="1"></GoodsList>
    </div>
    <div v-else-if="kkk==2">
        <GoodsList :goodsId="2"></GoodsList>
    </div>
    <div v-else-if="kkk==3">33333</div>
    <div v-else-if="kkk==4">4444</div>
    <div v-else-if="kkk==5">55555</div>
    <div v-else><GoodsList :goodsId="1"></GoodsList></div>
</div>
</template>
<script>
import Msg from './msg.js'
import GoodsList from './goodsList.vue'
export default {
  data () {
    return {
      kkk: 0
    }
  },
  mounted: function () {
    var _this = this
    Msg.$on('val', function (m) {
      _this.kkk = m
    })
  },
  components: {
    GoodsList
  }

}
</script>
