<template>
  <van-goods-action>
    <van-goods-action-icon icon="chat-o" text="客服" @click="onClickIcon"/>
    <van-goods-action-icon icon="cart-o" text="购物车" @click="onClickIcon"/>
    <van-goods-action-button type="warning" text="加入购物车" @click="onClickButton"/>
    <van-goods-action-button type="danger" text="立即购买" @click="onClickButton"/>
  </van-goods-action>
</template>

<script>
import Vue from 'vue'
import {
  Toast,
  GoodsAction,
  GoodsActionIcon,
  GoodsActionButton
} from 'vant'

Vue
  .use(GoodsAction)
  .use(GoodsActionIcon)
  .use(GoodsActionButton)
  .use(Toast)
export default {
  data () {
    return {}
  },
  methods: {
    onClickIcon () {
      Toast('点击图标')
    },
    onClickButton () {
      Toast('点击按钮')
    }
  }
}
</script>

<style scoped>

</style>
