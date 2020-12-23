<template>
  <div class="login">
    <div class="title">
      登录
    </div>
    <div class="form">
      <div>
        <input />
      </div>
      <div>
        <input />
        <span>获取验证码</span>
      </div>
    </div>
    <div class="login-btn">
      登录
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
      
        }
    },
};
</script>

<style scoped>
  .title {
    position: relative;
    padding-left: 28px;
    padding-top: 30px;
    font-size: 24px;
    font-family: PingFangSC-bold;
  }
  .title::after {
    content: '';
    width: 42px;
    height: 10px;
    line-height: 20px;
    border-radius: 16px;
    background-color: rgba(238, 8, 8);
    text-align: center;
    border: 1px solid rgba(255, 255, 255, 100);
    position: absolute;
    bottom: -5px;
    left: 30px;
    z-index: 9;
  }
  .form {
    padding: 45px 32px;
  }
  .login-btn {
    text-align: center;
    width: 194px;
    height: 36px;
    border-radius: 31px;
    background-color: rgba(238, 8, 8, 100);
    color: rgba(255, 255, 255, 100);
    font-size: 14px;
    margin: auto;
    font-family: Microsoft Yahei;
    border: 1px solid rgba(255, 255, 255, 100);
  }
</style>