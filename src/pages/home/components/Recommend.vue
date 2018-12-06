<template>
  <div>
    <div class="title">-热销推荐-</div>
    <ul>
      <li class="item" v-for="item of list" :key="item.id">
        <img :src="item.imgUrl"  alt="" class="item_img">
        <div class="item_info">
          <p class="item_title">{{item.title}}</p>
          <p class="item_sale">{{item.desc}}</p>
          <div class="item_song">
            <p class="item_qi">{{item.qi}}</p>
            <span>|</span>
            <p class="item_fei">{{item.fei}}</p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style scoped>
  .title{
    text-align: center;
    margin-top: .2rem;
    line-height: .8rem;
    text-indent: .2rem;
  }
  .item{
    overflow: hidden;
    display: flex;
    height: 1.9rem;
  }
  .item_img{
    width: 1.7rem;
    height: 1.7rem;
    padding: .1rem;
  }
  .item_info{
    flex: 1;
    padding: .1rem;
    min-width: 0;
  }
  .item_title{
    line-height: .54rem;
    font-size: .32rem;
  }
  .item_sale{
    margin-top: .2rem;
    line-height: .4rem;
    font-size: .10rem;
  }
  .item_song{
    margin-top: .2rem;
    width: 2.4rem;
    font-size: .06rem;
  }
  .item_qi{
    float: left;
    margin-right: .2rem;
  }
  .item_fei{
    float: right;
  }
</style>
