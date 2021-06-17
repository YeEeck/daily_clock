<template>
  <div class="home">
    <h1>签到器</h1>
    <login-reg></login-reg>
  </div>
</template>

<script>
import login_reg from "../components/Login_Reg.vue";

export default {
  name: "Home",
  data() {
    return {
    };
  },
  components: {
    "login-reg": login_reg,
  },
  methods: {
  },
};
</script>


<style lang="less">
.home {
  margin: 0;
  padding: 0;
  background-color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>