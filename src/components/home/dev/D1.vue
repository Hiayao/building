<template>
  <div class="swiper-container">
    <div class="all">
      <div class="left"></div>
      <div class="center">
        <swiper ref="mySwiper" :options="swiperOptions">
          <swiper-slide v-for="(item,index) in pics" :key="index">
            <img :src="item.picture_url" alt  class="pic"/>
          </swiper-slide>

          <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
        <div class="swiper-button-prev"></div>
        <!--左箭头。如果放置在swiper-container外面，需要自定义样式。-->
        <div class="swiper-button-next"></div>
        <!--右箭头。如果放置在swiper-container外面，需要自定义样式。-->
      </div>
      <div class="right"></div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";
import axios from "axios";
export default {
  name: "",
  props: {},
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      pics: [],
      swiperOptions: {
        pagination: {
          el: ".swiper-pagination"
        },
        autoplay: true,
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
          
        }
        // Some Swiper option/callback...
      }
    };
  },
  methods: {
    getData() {
      axios
        .get("http://120.78.14.107/api/v2/index/banner-pictures")
        .then(res => {
          this.pics = res.data;
          console.log(res.data);
        })
        .catch(err => {
          console.log(err);
        });
    }
  },
  mounted() {
    this.getData();
  },
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.all {
  width: 1240px;
  height: 380px;
  display: flex;
}
.left {
  width: 370px;
  height: 380px;
  background: pink;
}
.center {
  width: 720px;
  height: 380px;
}
.right {
  width: 150px;
  height: 380px;
  background: pink;
}
.swiper-container {
  --swiper-theme-color: #ffffff; /* 设置Swiper风格 */
  --swiper-navigation-color: #cdd6cf; /* 单独设置按钮颜色 */
  --swiper-navigation-size: 20px; /* 设置按钮大小 */
}

.swiper-button-prev {
    left:380px !important;
}
.swiper-button-next {
    right: 160px !important ;
}
.pic {
    width: 720px;
    height: 380px;
}
</style>