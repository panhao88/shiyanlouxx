<template>
  <div class="boh">
    <div class="kecheng">
      <div v-for="(item,index) in app" :key="index" class="kecheng1">
        <div class="kecheng3">
        {{item.name}}
        {{item.tags[0].name}}
        {{item.tags[1].name}}
        </div>
      </div>
      <div class="kecheng2">
        <div>
          <button style="border-radius: 20%; background: rgba(0,0,0,0.2); color: beige;">经管专区</button>
        </div>
      </div>
      <!-- ============================= -->
      <div>
        
      </div>
    </div>
    <swiper ref="mySwiper" :options="swiperOptions" class="swiper">
      <swiper-slide v-for="(item,index) in arr" :key="index" class="item">
        <div :style="{background:item.background_color}" class="left"></div>
        <img class="img" :src="item.picture_url" alt />
        <div :style="{background:item.background_color}" class="right"></div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
  </div>
</template>
<script>
import axios from "axios";
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";
export default {
  name: "",
  props: {
    arr: {
      type: Array
    },
    app: {
      type: Array
    }
  },
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      swiperOptions: {
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        observer: true,
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        },
        // 是否循环播放
        loop: true,
        autoplay: true
      }
    };
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {},
  filters: {}
};
</script>

<style scoped lang='scss'>
.boh {
  width: 100%;
  height: 350px;
  position: relative;
}

.img {
  position: absolute;
  right: 258px;
  width: 890px;
  height: 350px;
}
.left {
  // position: absolute;
  width: 45%;
  height: 350px;
  //  left: 0px;
}
.right {
  position: absolute;
  width: 20%;
  height: 350px;
  right: 0px;
}

.item {
  display: flex;
}
.kecheng {
  position: absolute;
  left: 225px;
  width: 12%;
  height: 350px;
  background: rgba(0, 0, 0, 0.2);
  z-index: 2;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
.kecheng1 {
  width: 160px;
  height: 42px;
  font-size: 10px;
  font-weight: 800;
  border-bottom: 1px solid beige;
  display: flex;
  flex-direction: column;
  // justify-content: center;
  justify-content: space-around;
  align-items: center;
  color: beige;
  
}

.kecheng :hover {
  color: black;
  background: cornsilk;
}
.swiper-button-prev {
  position: absolute;
  left: 29%;
  font-size: 5px;
  color: #fff;
}
.swiper-button-next {
  position: absolute;
  color: #fff;
  right: 17%;
}
.kecheng2 {
  width:160px ;
  height: 48px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.kecheng3{
  width: 160px;
overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
</style>