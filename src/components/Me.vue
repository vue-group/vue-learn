<template>
  <div id="me">
    <mt-header fixed :title="title" class="title"></mt-header>
    <div class="cell">
      <mt-cell title="未设置昵称" label="看车号：542341" is-link to="/userInfo" class="user">
        <img slot="icon" src="../assets/img-default-avatar.svg" class="avator">
        <img src="../assets/ico-qrcode.svg">
      </mt-cell>
    </div>
    <div class="item">
      <mt-cell title="我的车" is-link>
        <img slot="icon" src="../assets/me/ico-mycar.svg">
      </mt-cell>
      <mt-cell title="钱包" is-link>
        <img slot="icon" src="../assets/me/ico-wallet.svg">
      </mt-cell>
      <mt-cell title="卡券" is-link>
        <img slot="icon" src="../assets/me/ico-coupon.svg">
      </mt-cell>
    </div>
    <div>
      <mt-cell title="订单" is-link>
        <img slot="icon" src="../assets/me/ico-order.svg">
      </mt-cell>
    </div>
    <div class="item">
      <mt-cell title="设置" is-link to="/set" >
        <img slot="icon" src="../assets/me/ico-settings.svg">
      </mt-cell>
    </div>
  </div>
</template>
<script>
  import '../assets/styles/me-page.css'

  export default {
    name: 'me',
    data() {
      return {
        title: '我'
      }
    }
  }
</script>

<style scoped>
  #me {
    margin-top: 12px;
  }

  .title {
    height: 44px;
    font-size: 18px;
    color: #fff;
    background-color: #333;
  }

  .user {
    background-color: #fff;
  }

  .item {
   margin: 12px 0;
  }

  .avator {
    padding: 12px 2px;
    width: 56px;
    height: 56px;
  }
</style>
