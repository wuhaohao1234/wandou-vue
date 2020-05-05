<template>
  <div class="AddAddress">
    <!-- <van-popup show="{{ show }}" bind:close="onClose">内容</van-popup> -->
    <!-- <van-area area-list="{{ areaList }}" value="110101" /> -->
    <van-address-edit
      :area-list="areaList"
      show-delete
      show-set-default
      show-search-result
      :search-result="searchResult"
      :area-columns-placeholder="['请选择', '请选择', '请选择']"
      @save="onSave"
      @delete="onDelete"
      @change-detail="onChangeDetail"
    />
  </div>
</template>
<script>
import { Toast } from "vant";

import cityList from "../area.js";
export default {
  name: "AddAddress",
  data() {
    return {
      areaList: cityList,
      searchResult: []
    };
  },
  methods: {
    onSave() {
      Toast("save");
    },
    onDelete() {
      Toast("delete");
    },
    onChangeDetail(val) {
      if (val) {
        this.searchResult = [
          {
            name: "黄龙万科中心",
            address: "杭州市西湖区"
          }
        ];
      } else {
        this.searchResult = [];
      }
    }
  }
};
</script>
<style lang="scss">
</style>