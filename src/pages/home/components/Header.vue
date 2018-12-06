<template>
<div class="header">
    <div class="header_up">
      四川邮电职业技术学院
      <span class="iconfont">&#xe6aa;</span>
    </div>
    <div class="header_down">
      <span class="iconfont">&#xe632;</span>
      搜索饿了么商家、商品名称
    </div>
</div>
</template>

<script>
export default{
  name: 'HomeHeader'
}
</script>

<style scoped>
  .header{
    height: 1.7rem;
    background-color: #0af;
    color: #fff;
  }
  .header_up{
    width: 100%;
    overflow: hidden;
    padding-left: .2rem;
    padding-top: .23rem;
  }
  .header_down{
    overflow: hidden;
    margin-top: .34rem;
    padding-left: .2rem;
    margin-right: .2rem;
    background: #fff;
    border-radius: .1rem;
    height: .64rem;
    line-height: .64rem;
    margin-left: .2rem;
    color: #999;
  }
  .back_icon{
    text-align: center;
    }
</style>
