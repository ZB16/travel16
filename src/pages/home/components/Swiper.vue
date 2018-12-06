<template>
  <div class="wrapper">
    <div class="rob">
        <div class="rob_left">
           <div class="rob_box">
              <h3 class="rob_title">品质套餐</h3>
              <p class="rob_desc">搭配齐全吃得好</p>
              <a class="rob_li"><p>立即抢购></p></a>
              <img class="rob_img" src="https://fuss10.elemecdn.com/d/d4/16ff085900d62b8d60fa7e9c6b65dpng.png?imageMogr/thumbnail/!240x160r/gravity/Center/crop/240x160/">
           </div>
        </div>
        <div class="rob_right">
            <div class="rob_box">
              <h3 class="rob_title">品质套餐</h3>
              <p class="rob_desc">搭配齐全吃得好</p>
              <a class="rob_li"><p>立即抢购></p></a>
              <img class="rob_img" src="https://fuss10.elemecdn.com/d/d4/16ff085900d62b8d60fa7e9c6b65dpng.png?imageMogr/thumbnail/!240x160r/gravity/Center/crop/240x160/">
            </div>
        </div>
    </div>
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in list" :key="item.id">
        <img class="swiper_img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default{
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  }
}
</script>

<style scoped>
.rob{
  width: 100%;
  height: 3rem;
}
.rob_left{
  width: 50%;
  float: left;
}
.rob_right{
  width: 50%;
  float: right;
}
.rob_box{
  width: 80%;
  margin: 0 auto;
  overflow: hidden;
  padding: .2rem 0;
  background: #f4f4f4;
}
.rob_title{
  margin-left: .2rem;
}
.rob_desc{
  margin-left: .2rem;
  margin-top: .2rem;
  font-size: .12rem;
}
.rob_li{
  margin-left: .2rem;
}
.rob_li p{
  margin-left: .2rem;
  font-size: .12rem;
}
.rob_img{
  width: 2rem;
  float: right;
}
  .swiper_img{
    width: 100%;
  }
  .wrapper >>> .swiper-pagination-bullet-active{
    background: #fff !important
  }
</style>
