<template>
  <div>
    <van-card
      num="2"
      price="2.00"
      desc="描述信息"
      title="商品标题"
      thumb="https://img.yzcdn.cn/vant/t-thirt.jpg"
    >
      <div slot="tags">
        <van-tag plain type="danger">标签</van-tag>
        <van-tag plain type="danger">标签</van-tag>
      </div>
      <div slot="footer">
        <van-button size="mini">按钮</van-button>
        <van-button size="mini">按钮</van-button>
      </div>
    </van-card>
    <van-goods-action>
      <van-goods-action-icon icon="chat-o" text="客服" @click="onClickIcon"/>
      <van-goods-action-icon icon="cart-o" text="购物车" @click="onClickIcon"/>
      <van-goods-action-button type="warning" text="加入购物车" @click="onClickButton"/>
      <van-goods-action-button type="danger" text="立即购买" @click="onClickButton"/>
    </van-goods-action>
  </div>
</template>

<script>
import Vue from 'vue'
import {
  Toast,
  GoodsAction,
  GoodsActionIcon,
  GoodsActionButton,
  Card,
  Button,
  Tag
} from 'vant'

Vue
  .use(GoodsAction)
  .use(GoodsActionIcon)
  .use(GoodsActionButton)
  .use(Toast)
  .use(Card)
  .use(Button)
  .use(Tag)
export default {
  name: 'Items',
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
