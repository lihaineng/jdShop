<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont position__icon">图标1</span>
      北京理工大学国防科技园2号楼10层
      <span class="iconfont position__notice">图标2</span>
    </div>
    <div class="docker">
      <div class="docker__item">
          <div class="iconfont"></div>
          <div class="docker__title">首页</div>
      </div>
      <div class="docker__item">
          <div class="iconfont"></div>
          <div class="docker__title">购物车</div>
      </div>
      <div class="docker__item">
          <div class="iconfont"></div>
          <div class="docker__title">订单</div>
      </div>
      <div class="docker__item">
          <div class="iconfont"></div>
          <div class="docker__title">我的</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import './style/viriables.scss';
@import './style/mixins.scss';
// .wrapper {
//   position: absolute;
//   left: 0;
//   top: 0;
//   right: 0;
//   bottom: .5rem;
//   padding: 0 .18rem;
// }
// .position {
//    position: relative;
// }
.docker {
  display: flex;
  // box-sizing: border-box;
  position: absolute;
  // padding: 0 .18rem;
  left: 0;
  bottom: 0;
  width: 100%;
  height: .49rem;
  border-top: .01rem solid #F1F1F1;
  background: green;
  &__item {
    flex: 1;
    text-align: center;
  }
}
</style>
