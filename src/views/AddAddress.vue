<template>
  <div class="AddAddress">
    <van-field v-model="value" placeholder="收货人" />
    <van-field v-model="value" placeholder="手机号码" />

    <van-field v-model="value" placeholder="所在地区" />

    <van-field v-model="value" type="textarea" placeholder="详细地址" />

    <van-field v-model="value" placeholder="设为默认地址" />
  </div>
</template>
<script>
export default {
  name: "AddAddress",
  created() {
    console.log(1);
  },
  data() {
    return {
      value: ""
    };
  },
  methods: {}
};
</script>
<style lang="scss">
</style>