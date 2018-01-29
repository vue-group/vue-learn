<template>
  <div class="user-info">
    <mt-header fixed :title="title" class="title">
      <router-link :to="{path: '/', meta: {tab: 'tab4'}}" slot="left">
        <mt-button icon="back">设置</mt-button>
        <!--<mt-button @click="handleClose">我</mt-button>-->
      </router-link>
    </mt-header>
    <div class="list">
      <mt-cell title="账户安全" is-link ></mt-cell>
    </div>
    <div class="list">
      <mt-cell title="实名认证" is-link ></mt-cell>
      <mt-cell title="车主认证" is-link ></mt-cell>
    </div>
    <div class="list">
      <mt-cell title="我的地址" is-link ></mt-cell>
    </div>
    <div class="list">
      <mt-cell title="法律条款" is-link ></mt-cell>
      <mt-cell title="关于我们" is-link ></mt-cell>
    </div>
    <div class="list">
      <button class="mint-button mint-button--default mint-button--large" @click = "test"><!---->
        <label class="mint-button-text">退出登录</label>
      </button>
    </div>
  </div>
</template>

<script>
  import { MessageBox } from 'mint-ui';
  import '../assets/styles/user-info.css'
  export default {
    name: "Setting",
    data() {
      return {
        title: "设置"
      }
    },methods:{
      test(){
        MessageBox({
          title: '您确定退出？',
          message: '退出将会删除您的个人数据。',
          showCancelButton: true
        });
      }
    }
  }




</script>

<style scoped>
  .user-info {
    margin-top: 44px;
  }

  .title {
    height: 44px;
    font-size: 18px;
    color: #fff;
    background-color: #333;
  }

  .list {
    margin: 12px 0;
  }

  .mint-button-text {
    color: #5bafff;
  }

</style>
