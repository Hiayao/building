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
          <div class="Ab">社区 ▼</div>
        </div>
        <div class="ul">
          <ul class="ul1">
            <br />
            <li class="li">讨论</li>
            <li class="li">教程库</li>
            <li class="li">直播</li>
            <li class="li" style="border-radius: 0px 0px 5px 5px;">比赛</li>
          </ul>
        </div>
        <div class="Ac">
          <input type="text" placeholder="搜索 课程/问答" class="ipt" />
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
.ul {
  width: 70px;
  height: 50px;
  // z-index: 3;
  position: absolute;
  right: 370px;
	
}
.li {
  display: none;
  width: 120px;
  background: white;
  line-height: 34px;
  margin-left: -40px;
  padding-left: 14px;
	box-shadow: 0px 15px 25px 15px rgb(247, 247, 247)
}

.li:hover {
  background: rgb(219, 214, 214);
}
.b3 {
  width: 100px;
  line-height: 40px;
  padding-left: 35px;
}
.ul:hover .li {
  display: block;
}
</style>