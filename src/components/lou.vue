<template>
  <div class="box">
    <div>
      <slot name="to"></slot>
    </div>
    <div>
      <slot name="do"></slot>
    </div>
    <div class="box1">
     <div>
        <span class="bor">楼+ 实战课程 |</span>
      <span>定期开班，导师助教全程辅导，最快最优成长</span>
     </div>
      <div>更多></div>
    </div>
    <div class="box2">
      <div v-for="(item,index) in akk" :key="index" class="box3">
        <div v-if="index < 4" class="bot">
          <div class="bot1" >
            <div class="bot2">
              <img class="img" :src="item.picture_url" alt />
            </div>
            <div class="bot3">{{item.title}}</div>
            <div>{{item.open_time}}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {
    akk: {
      type: Array
    }
  },
  components: {},
  data() {
    return {};
  },
  methods: {},
  mounted() {},
  watch: {},
  computed: {},
  filters: {}
};
</script>

<style scoped lang='scss'>
.box {
  width: 866px;
  height: 180px;
  // border: solid 1px black;
  display: flex;
}
.box1 {
  width: 866px;
  height: 50px;
  // border: solid 1px black;
  justify-content: space-between;
  align-items: center;
  display: flex;
}
.box2 {
  width: 866px;
  height: 150px;
  // background: chartreuse;
  display: flex;
  align-items: center;
  justify-content: center;
  justify-content: space-around;
}
// .bot1 {
//   // background: blueviolet;
// }
.bot {
  width: 210px;
  height: 134px;
  // border: solid 1px black;
  border-radius: 20px 20px 0px 0px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
.bot3 {
  width: 160px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.img {
  width: 210px;
  height: 60px;
}
.bor {
  font-size: 25px;
}
.bot :hover{
   box-shadow: 0 1px 50px 0 red;
   
}

</style>