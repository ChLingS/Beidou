<template>
  <div class="all">
    <div class="nihao">
        <div class="headermid">
          <div class="centertext">北斗湿地守护者</div>
        </div>
    </div>
    <div class="carousel">
      <n-carousel draggable>
        <img class="carousel-img" src="https://p2.itc.cn/q_70/images03/20230525/e42e6f5448c24fa7ad840c333221ccff.png">
        <img class="carousel-img" src="https://p9.itc.cn/q_70/images03/20230525/58678a87dca540b6b995507198b91bb8.jpeg">
      </n-carousel>
    </div>
    <div class="selectID">
        请选择身份
      <div class="cardpos">
        <n-card title="生态小白&nbsp;>" size="huge" @click="xiaobai">
          通过观察来监测湿地生态
        </n-card>
        <NDivider/>
        <n-card title="我是高手&nbsp;>" size="huge">
          具有一定设备以及相关知识
        </n-card>
      </div>

    </div>
    <div class="menu">
      <n-space justify="space-around" size="large">
        <n-button quaternary bordered='flase' class="headerButton">首页</n-button>
        <n-button quaternary bordered='flase' class="headerButton">地图</n-button>
        <n-button quaternary bordered='flase' class="headerButton">个人</n-button>
      </n-space>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import { NButton, NSpace, NCarousel, NCard, NDivider } from 'naive-ui'

export default defineComponent({
  components: {
    NButton,
    NSpace,
    NCarousel,
    NCard,
    NDivider,
  },
  methods:{
    xiaobai(){
      console.log("1")
    }
  }
})
</script>
<style>
@font-face {
  font-family: 'SourceHanSansCN-Medium';
  src: url('/fontfamily/SourceHanSansCN-Medium.55379b93.woff') format('woff');
}
.menu {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 1rem;
  background-color: rgb(6, 255, 168);
  border-radius: 10px; /* 添加圆角样式 */
}

.headerButton {
  height: 1rem;
  position: relative;
  display: flex;
  /* top: 0%; */
  font: 0.7em sans-serif;
}

.all {
  display: flex;
  /* height: 844px; */
}

.nihao {
  display: flex;
  position: relative;
  top: 0%;
  font: 1em sans-serif;
  font-size: 0.5rem;
  background-color: aquamarine;
  border-radius: 10px 10px 0 0;
  width: 100%;
  height: 1rem;
}
.carousel-img {
  width: 100%;
  height: 240px;
  object-fit: cover;
  border-radius:0 0 10px 10px ;
}
.carousel{
  display: flex;
  position: absolute;
  margin-top: 1rem;
}
.selectID{
  display: flex;
  position: absolute;
  margin-top: 7.5rem;
  font-size: 0.5rem;
  width: 100%;
  /* font-family: SourceHanSansCN-Medium; */
}
.cardpos{
  display: block;
  position: absolute;
  margin-top: 1rem;
  width: 100%;
  /* font-family: SourceHanSansCN-Medium; */
}
.headermid{
  display: flex;
  justify-content: center;
  align-items: center;
}
.centertext{
  text-align: center;
  position: relative;
  left:90%;
  font-family: SourceHanSansCN-Medium;
}
</style>