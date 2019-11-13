<template>
  <div>
    <van-nav-bar
      :title=headTitle
      :left-text=leftText
      right-text="按钮"
      left-arrow
      @click-left="onClickLeft"
      @click-right="onClickRight"
    />
    <van-card
      num="2"
      price="2.00"
      desc="9102年新款"
      title="短袖"
      thumb="https://img.yzcdn.cn/vant/t-thirt.jpg"
    >
      <div slot="tags">
        <van-tag plain type="danger">修身</van-tag>
        <van-tag plain type="danger">养性</van-tag>
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
  Tag,
  NavBar
} from 'vant'

Vue
  .use(GoodsAction)
  .use(GoodsActionIcon)
  .use(GoodsActionButton)
  .use(Toast)
  .use(Card)
  .use(Button)
  .use(Tag)
  .use(NavBar)
export default {
  name: 'Items',
  data () {
    return {
      headTitle: '大甩卖',
      leftText: '返回'
    }
  },
  methods: {
    onClickIcon () {
      Toast('点击图标')
    },
    onClickButton () {
      Toast('点击按钮')
    },
    onClickLeft () {
      Toast(this.leftText)
    },
    onClickRight () {
      Toast('按钮')
    }
  }
}
</script>

<style scoped>

</style>
