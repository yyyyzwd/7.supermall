<template>
  <div id="detail_bottom_bar">
    <div class="bottom_left">
      <div class="service">
        <i class="icon"></i>
        <span>客服</span>
      </div>
      <div class="shop">
        <i class="icon"></i>
        <span>店铺</span>
      </div>
      <div class="collect">
        <i class="icon"></i>
        <span>收藏</span>
      </div>
    </div>
    <div class="bottom_right">
      <div class="cart" @click="addToCart">
        加入购物车
      </div>
      <div class="buy">
        购买
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "DetailBotBar",
    methods:{
      //点击添加购物车
      addToCart(){
        this.$emit('addEvent');
      }
    }
  }
</script>

<style scoped>
  #detail_bottom_bar {
    font-size: 1px;
    display: flex;
    position: fixed;
    background-color: #fff;
    bottom: 0px;
    left: 0;
    right: 0;
    height: 44px;
    text-align: center;
    box-shadow: 0 -0.04rem 0.4rem gray;
  }
  .bottom_left {
    display: flex;
    flex: 1;
  }
  .bottom_left > div {
    flex: 1;
    border-right: 0.04rem solid rgba(128, 128, 128, 0.2);
    line-height: 15px;
    padding-top: 5px;
  }
  .bottom_left .icon {
    display: block;
    background: url("~@/assets/img/detail/detail_bottom.png") 0 0/100%;
    width: 1rem;
    height: 1rem;
    margin: 0.12rem auto;
  }
  .service .icon {
    background-position: 0 -2.4rem;
  }
  .shop .icon {
    background-position: 0 -4.5rem;
  }
  .bottom_right {
    display: flex;
    flex: 1;
  }
  .bottom_right > div {
    flex: 1;
    line-height: 44px;
  }
  .cart {
    background-color: rgb(255, 174, 0);
    color: #ffffff;
  }
  .buy {
    background-color: var(--color-tint);
    color: white;
  }
</style>