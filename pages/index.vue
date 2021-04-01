<template>
  <div class="container">
    <div>
      <van-nav-bar title="检证案例" >
            <template #left>
                
            </template>
            <template #right>
                <van-icon name="more-o" size="18" @click="onClickIcon"/>
            </template>
        </van-nav-bar>
      <van-list
        v-model="loading"
        :finished="finished"
        finished-text="no more"
        @load="onLoad"
      >
        <!-- <van-cell v-for="item in list" :key="item" :title="item" /> -->
        <NuxtLink to="/detail" v-for="item in list" :key="item">
          <van-card
            num="2"
            price="2.00"
            desc="描述信息"
            title="商品标题"
            thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
          >
            <template #tags>
              <van-tag plain type="danger">标签</van-tag>
              <van-tag plain type="danger">标签</van-tag>
            </template>
            <template #footer>
              <van-button size="mini">按钮</van-button>
              <van-button size="mini">按钮</van-button>
            </template>
          </van-card>
        </NuxtLink>
      </van-list>

      <van-overlay :show="show" @click="onClickButton">
          <div class="wrapper" >
              <div class="block">{{temptext}}</div>
          </div>
      </van-overlay>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
export default {
  components: {
    Logo
  },
  data() {
    return {
      list: [],
      loading: false,
      finished: false,
      show: false,
      temptext: '第一次载入时，检证Line Login功能',
    };
  },
  mounted(){
    this.show = true;
  },
  methods: {
    onLoad() {
      // 异步更新数据
      // setTimeout 仅做示例，真实场景中一般为 ajax 请求
      setTimeout(() => {
        for (let i = 0; i < 10; i++) {
          this.list.push(this.list.length + 1);
        }

        // 加载状态结束
        this.loading = false;

        // 数据全部加载完成
        if (this.list.length >= 40) {
          this.finished = true;
        }
      }, 1000);
    },
    onClickButton() {
      // Toast('点击图标');
      this.show = false;
    },
    onClickIcon() {
      // Toast('点击图标');
      this.show = true;
      this.temptext = 'Notify的ICON，检证Line Notify功能';
    },
  },
}
</script>

<style scoped>
/* .container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
} */


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
</style>
