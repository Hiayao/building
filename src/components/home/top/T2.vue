<template>
  <div>
    <div class="All">
      <div class="A1">
        <div>
          <img src="../../../../图片/QQ截图20200601125808.png" alt class="imge" />
        </div>
        <div style="margin-left:3px ;">全部课程</div>
      </div>
      <div class="A2">
        <div class="Aa">
          <div class="Ab">路径</div>
          <div class="Ab">训练营</div>
          <div class="Ab">楼+</div>
          <div class="Ab">
            <div>会员</div>
            <div>
              <img src="https://static.shiyanlou.com/frontend/dist/img/02a4001.svg" alt class="hot" />
            </div>
          </div>
          <div class="b1">
            <div class="Ab">社区 ▼</div>
            <div class="b2">
              <div class="b3">讨论</div>
              <div class="b3">教程库</div>
              <div class="b3">直播</div>
              <div class="b3">比赛</div>
            </div>
          </div>
        </div>
        <div class="Ac">
          <input type="text" placeholder="搜索 课程/问答" class="ipt" />
          <div class="big">
            <i class="iconfont icon-sousuo item3"></i>
          </div>
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
  computed: {}
};
</script>

<style scoped lang='scss'>
.All {
  width: 100%;
  height: 50px;
  display: flex;
  position: relative;
}
.A1 {
  display: flex;
  align-items: center;
  font-size: 13px;
  color: white;
  width: 220px;
  height: 50px;
  background: #08bf91;
  position: absolute;
  left: 150px;
}
.A1:hover {
  cursor: pointer;
}
.imge {
  height: 16px;
  width: 20px;
  margin-left: 8px;
}
.A2 {
  display: flex;
  // justify-content: center;
  align-items: center;
  width: 720px;
  height: 50px;
  background: white;
  position: absolute;
  right: 150px;
  font-size: 13px;
}
.Aa {
  height: 50px;
  display: flex;
  position: absolute;
  left: 0px;
}
.Ab {
  width: 70px;
  height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}
.Ab:hover {
  color: #08bf91;
  cursor: pointer;
}
.Ac {
  position: absolute;
  right: 100px;
  height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.big {
  position: absolute;
  right: -80px;
}
.big:hover {
  cursor: pointer;
}
.hot {
  position: absolute;
  top: 10px;
  padding-left: 8px;
}
.ipt {
  border: 1px solid #999;
  border-radius: 4px 4px 4px 4px;
  position: absolute;
  padding: 5px;
}
.ipt:hover {
  border: 1px solid #08bf91;
}
.ipt:focus {
  //点击后输入框的变化
  outline: none; //点击后输入框的边框
  border: 1px solid #08bf91;
}
.b1 {
  cursor: pointer;
}
.b2 {
  margin-left: -20px;
  position: absolute;
  background: #ffffff;
  display: none;
  border-radius: 0px 0px 5px 5px;
  box-shadow: 0px 15px 25px 15px rgba(247, 247, 247, 0.4);
  z-index: 3;
}
.b3 {
  width: 100px;
  line-height: 40px;
  padding-left: 35px;
}
.b1:hover > .b2 {
  display: block;
}
.b3:hover {
  background: rgb(241, 241, 241);
  color: #08bf91;
}
</style>