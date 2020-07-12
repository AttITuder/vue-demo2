<template>
  <div>
    <div class="title">热门推荐</div>
    <ul class="menu">
      <li @click="menu1">笔记本电脑</li>
      <li @click="menu2">手机</li>
      <li @click="menu3">服饰</li>
      <li @click="menu4">手表</li>
      <li @click="menu5">书籍</li>
      <li @click="menu6">玩具</li>
      <li @click="menu7">家电</li>
      <li @click="menu8">学习用品</li>
      <li @click="menu9">办公用品</li>
      <li @click="menu10">旅行用品</li>
    </ul>
  </div>
</template>
<style>
.title {
  width: 100px;
  color: red;
}
.menu li {
  list-style: none;
  background-color: white;
  margin-bottom: 2px;
  height: 50px;
  line-height: 50px;
  cursor: pointer;
}
</style>
<script>
import Msg from './msg.js'
export default {
  methods: {
    menu1: function () {
      Msg.$emit('val', '1')
    },
    menu2: function () {
      Msg.$emit('val', '2')
    },
    menu3: function () {
      Msg.$emit('val', '3')
    },
    menu4: function () {
      Msg.$emit('val', '4')
    },
    menu5: function () {
      Msg.$emit('val', '5')
    },
    menu6: function () {
      Msg.$emit('val', '6')
    },
    menu7: function () {
      Msg.$emit('val', '7')
    },
    menu8: function () {
      Msg.$emit('val', '8')
    },
    menu9: function () {
      Msg.$emit('val', '9')
    },
    menu10: function () {
      Msg.$emit('val', '10')
    }
  }
}
</script>
