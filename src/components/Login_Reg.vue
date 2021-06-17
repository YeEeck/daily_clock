<template>
  <div class="login_reg_out">
    <div class="com_title">
      {{ title }}
    </div>
    <y-input v-model="outData" class="input1"></y-input>
    <input type="text" v-model="outData">
  </div>
</template>

<script>
import y_input from "./input.vue";

export default {
  name: "login-reg",
  data() {
    return {
      isLogin: true,
      outData: ""
    };
  },
  components: {
    "y-input": y_input,
  },
  computed: {
    title() {
      if (this.isLogin) {
        return "登录";
      } else {
        return "注册";
      }
    },
  },
};
</script>

<style lang="less">
.com_title{
    text-align: center;
}
.input1{
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
    width: 10rem;
    height: 1.5rem;
}
</style>