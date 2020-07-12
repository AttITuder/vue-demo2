<template>
  <div class="main">
    <div class="left">
      <Left></Left>
    </div>
    <div class="right">
      <div class="top">
        <img src="img/banner1.jpg" />
      </div>
      <div class="bottom">
        <Right></Right>
      </div>
    </div>
  </div>
</template>
<style>
* {
  padding: 0px;
  margin: 0px;
}
.left {
  width: 100px;
  float: left;
  margin-right: 10px;
}
.right {
  width: 1000px;
  float: left;
  margin-left: 10px;
}
.main {
  width: 1200px;
  margin: 20px auto;
}
.top img {
  width: 1000px;
  height: 200px;
}
.left,
.right {
  background-color: #f5f5f5;
  height: 500px;
}
</style>
<script type="text/javascript">
import Left from '../components/Left.vue'
import Right from '../components/Right.vue'
export default {
  components: {
    Left,
    Right
  }
}
</script>
