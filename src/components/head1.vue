<template>
  <div>
    <div class="box">
      <div class="box1">
        <img src="../assets/QQ图片20200702101852.png" alt />
        <div>做实验，学编程</div>
      </div>
      <div class="box2">
        <div>企业版 | 学校版</div>
        <div>登录</div>
        <button style=" background: #08bf91;" class="zhuce">注册</button>
      </div>
    </div>
    <div class="bot">
      <div class="bot1">
        <i class="iconfont icon-chanpinguanli">全部课程</i>
      </div>
      <div class="bot2">
        <div class="bota">路径</div>
        <div class="botb">训练营</div>
        <div class="botc">楼+</div>
        <div class="botd">会员</div>
         <div class="todo">
           <div>
             <div class="bote">社区 <i class="iconfont icon-xiala"></i></div>
           </div>
        <div class="toyou">
          <div>讨论</div>
          <div>教程库</div>
          <div>直播</div>
          <div>比赛</div>
        </div>
      </div>
      </div> 
      <div class="bot3">
        <div>
          <input type="text" placeholder="搜索 课程、问答" class="ipt" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  props: {},
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
  height: 67px;
  display: flex;
  justify-content: space-between;
}
.box1 {
  width: 210px;
  height: 67px;
  justify-content: space-between;
  display: flex;
  align-items: center;
  font-weight: 800;
}
.box1 :hover {
  cursor: pointer;
  
  color: #08bf91;
}
.box2 :hover {
  cursor: pointer;
  color: #08bf91;
}
.zhuce:hover{
  color: beige;
}
.zhuce{
  border: none;
}
.box2 {
  width: 240px;
  height: 67px;
  justify-content: space-between;
  display: flex;
  align-items: center;
  font-size: 15px;
  font-weight: 800;
}
.bot {
  width: 886px;
  height: 50px;
  display: flex;
  // background: beige;
  position: relative;
}
.bot1 {
  width: 160px;
  height: 50px;
  color: beige;
  background: #08bf91;
  display: flex;
  align-items: center;
  font-weight: 800;
}
.bot1:hover{
  cursor: pointer;
}
.bot2 {
  width: 300px;
  height: 50px;
  display: flex;
  justify-content: space-around;
  align-items: center;
   font-size: 15px;
  font-weight: 800;
}
.bota:hover{
  color: #08bf91;
  cursor: pointer;
}
.botb:hover{
  color: #08bf91;
  cursor: pointer;
}
.botc:hover{
  color: #08bf91;
  cursor: pointer;
}
.botd:hover{
  color: #08bf91;
  cursor: pointer;
}
.bote:hover{
  color: #08bf91;
  cursor: pointer;
}
.bot3 {
  width: 250px;
  height: 50px;
  display: flex;
  align-items: center;
  position: absolute;
  right: 10px;
}

input {
  
  border: none;
  background-image: url("../assets/sou-suo.svg");
  background-position: right;
  background-repeat: no-repeat;
}
.todo {
  display: flex;
  position: relative;
}
.toyou {
  width: 80px;
  height: 100px;
  background: beige;
  position: absolute;
  top: 20px;
  z-index: 2;
   display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #fff;
  // border: solid 1px black;
  display: none;
}
.todo:hover .toyou {
  display: block;
  color: #08bf91; 
}
.toyou :hover{
  background: bisque;
}
</style>    