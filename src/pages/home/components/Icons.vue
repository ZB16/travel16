<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon_img">
            <img class="icon_img_style" :src="item.imgUrl" alt="">
          </div>
          <p class="icon_desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default{
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
        // loop: true
      }
    }
  },
  computed: {
    pages: function () {
      const pages = []
      this.list.forEach(function (item, index) {
        const page = Math.floor(index / 10)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style scoped>
  .icons >>> .swiper-container{
    overflow: hidden;
    height: 0;width: 100%;
    padding-bottom: 55%;
    /* background-color: green; */
  }
  .icon{
    position: relative;
    overflow: hidden;
    float: left;
    height: 0;
    width: 20%;
    padding-bottom: 25%;
    /* background-color: red; */
  }
  .icon_img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: .44rem;
    /* background-color: blue; */
    /* padding: .1rem; */
  }
  .icon_img_style{
    display: block;
    height: 100%;
    margin: 0 auto;
  }
  .icon_desc{
    font-size: 12px;
    position: absolute;
    bottom: 0;left: 0;right: 0;
    height: .44rem;
    line-height: .44rem;
    text-align: center;
    color: #333;
  }
</style>
