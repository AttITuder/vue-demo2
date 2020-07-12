<template>
  <div name="show">
    <ul>
      <li class="goodsList" v-for="goods in List" :key="goods.goodsName">
        <img v-bind:src="goods.img" />
        <p>{{goods.goodsName}}</p>
      </li>
    </ul>
  </div>
</template>
<style>
.goodsList {
  width: 200px;
  height: 200px;
  float: left;
  list-style: none;
  color: red;
  font-size: 9px;
  margin-bottom: 30px;
}
.goodsList img {
  width: 180px;
  height: 180px;
}
</style>
<script>
export default {
  name: 'show',
  data () {
    var obj = this
    var url = ''
    if (obj.goodsId === 1) {
      url = 'json/computer.json'
    } else if (obj.goodsId === 2) {
      url = 'json/shouji.json'
    } else {
      url = 'json/computer.json'
    }
    this.$http.get(url).then(function (res) {
      obj.List = res.data
    })
    return {
      List: []
    }
  },
  props: {
    goodsId: Number
  },
  watch: {
    goodsId () {
      var obj = this
      var url = ''
      if (obj.goodsId === 1) {
        url = 'json/computer.json'
      } else if (obj.goodsId === 2) {
        url = 'json/shouji.json'
      } else {
        url = 'json/computer.json'
      }
      this.$http.get(url).then(function (res) {
        obj.List = res.data
      })
      return {
        List: []
      }
    }
  }
}
</script>
