<template>
  <div class="home">
    <van-cell is-link>新增收获地址</van-cell>
    <van-swipe-cell>
      <van-cell is-link>某某某店铺</van-cell>
      <van-card
        num="2"
        price="2.00"
        :desc="description"
        title="商品标题"
        class="goods-card"
        thumb="https://img.yzcdn.cn/vant/cat.jpeg"
      />
      <template #right>
        <van-button square text="删除" type="danger" class="delete-button" />
      </template>

      <van-field v-model="discount" is-link placeholder="暂无可用" label="优惠卷：" />

      <van-field v-model="message" is-link placeholder="选填，给店家留言" label="店铺备注：" />
    </van-swipe-cell>

    <van-cell>
      商品总额：
      <div class="van-card__price">
        <div>
          <span class="van-card__price-currency">¥</span>
          <span class="van-card__price-integer">2</span>.
          <span class="van-card__price-decimal">00</span>
        </div>
      </div>
    </van-cell>
    <van-cell>
      运费：
      <div class="van-card__price">
        <div>
          <span class="van-card__price-currency">¥</span>
          <span class="van-card__price-integer">2</span>.
          <span class="van-card__price-decimal">00</span>
        </div>
      </div>
    </van-cell>
    <van-cell>
      优惠金额：
      <div class="van-card__price">
        <div>
          <span class="van-card__price-currency">¥</span>
          <span class="van-card__price-integer">2</span>.
          <span class="van-card__price-decimal">00</span>
        </div>
      </div>
    </van-cell>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
  data() {
    return {
      description: "我是某某商品我是某某商品我是某某商品我是某某商品是某某商品",
      show: false,
      value: "",
      discount: "",
      message: ""
    };
  }
};
</script>
<style lang="scss">
.goods-card {
  margin: 0;
  background-color: #fff;
}

.delete-button {
  height: 100%;
}

.home {
  .van-card__price {
    color: #e68f67;
  }
}
.van-cell {
  .van-cell__value {
    .van-card__price {
      float: right;
    }
  }
}
.van-card__bottom {
  .van-card__price {
    float: left;
  }
  .van-card__num {
    float: right;
  }
}
</style>