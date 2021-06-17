<template>
  <div class="outer">
    <input type="text" v-model="value" class="input_main" />
  </div>
</template>

<script>
export default {
  name: "y-input",
  data() {
    return {};
  },
  props: {
    value: String,
  },
  watch: {
    value() {
      this.text = this.value;
      try {
        this.$emit("input", this.text);
        this.$emit("change", this.text);
      } catch (e) {
        this.$emit("error", true);
      }
    },
  },
  methods: {},
};
</script>

<style lang="less">
.input_main {
  width: 100%;
  height: 100%;
  outline: none;

  background-color: rgb(250, 250, 250);

  padding-left: 0.5rem;
  border-radius: 5px;
  border-style: none;
  box-shadow: 0px 0px 3px lightgray;
  transition: box-shadow 0.7s;
  &:focus {
    box-shadow: 0px 0px 3px gray;
    transition: box-shadow 0.7s;
  }
}
</style>