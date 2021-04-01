<template>
    <div>
        <van-nav-bar title="检证案例" left-text="返回" left-arrow>
            <template #left>
                <nuxt-link to="/">
                    <van-icon name="revoke" size="18" />
                </nuxt-link>
            </template>
            <template #right>
                <van-icon name="share-o" size="18" @click="onClickIcon"/>
            </template>
        </van-nav-bar>
        <van-swipe :autoplay="3000">
            <van-swipe-item v-for="(image, index) in images" :key="index">
                <img v-lazy="image" style="height: 300px"/>
            </van-swipe-item>
        </van-swipe>
        <img v-lazy="'https://img01.yzcdn.cn/vant/apple-1.jpg'"  style="width: 100%"/>
        <img v-lazy="'https://img01.yzcdn.cn/vant/apple-1.jpg'"  style="width: 100%"/>
        <van-goods-action class="van-goods-action">
            <van-goods-action-icon icon="chat-o" text="message" @click="onClickMessaging" />
            <van-goods-action-icon icon="cart-o" text="购物车"  />
            <van-goods-action-icon icon="shop-o" text="店铺"  />
            <van-goods-action-button
                type="primary"
                text="Pay Now"
                @click="onClickPay"
            />
        </van-goods-action>

        <van-overlay :show="show" @click="onClickButton">
            <div class="wrapper" >
                <div class="block">{{temptext}}</div>
            </div>
        </van-overlay>
    </div>
</template>

<script>

import { Toast } from 'vant';

export default {
    data() {
        return {
            show: false,
            temptext: '',
            images: [
                'https://img01.yzcdn.cn/vant/apple-1.jpg',
                'https://img01.yzcdn.cn/vant/apple-2.jpg',
            ],
        }
    },
    methods: {
        onClickIcon() {
            // Toast('点击图标');
            this.temptext = '检证Line Social Plugins功能';
            this.show = true;

        },
        onClickMessaging() {
            // Toast('点击图标');
            this.temptext = '检证Line Messing功能';
            this.show = true;

        },
        onClickPay() {
            // Toast('点击图标');
            this.temptext = '检证Line Pay功能';
            this.show = true;

        },
        onClickButton() {
            // Toast('点击按钮');
            this.show = false;
        },
    },
};
</script>

<style scoped>

.my-swipe .van-swipe-item {
    color: #fff;
    font-size: 20px;
    line-height: 150px;
    text-align: center;
    background-color: #39a9ed;
  }

  .wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
  }

  .block {
    width: 120px;
    height: 120px;
    align-items: center;
    justify-content: center;
    background-color: #fff;
  }

  .van-goods-action{
      margin-bottom: 50px;
  }
</style>
