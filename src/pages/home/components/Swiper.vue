<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/1a23156781dc1399289e13eb984660f8.jpg_845x388_ed844e21.jpg'
      }, {
        id: '0002',
        imgUrl: '//mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/5bd701f48397f26899e36e26da02fb17.jpg_845x388_ba76d191.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 45.75%
    .swiper-img
      width: 100%
</style>
