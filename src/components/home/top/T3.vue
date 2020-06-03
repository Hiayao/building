<template>
  <div>
    <div class="All" :class="navBarFixed == true ? 'navBarWrap' :''">
        <!-- 将需要固定的元素的class与navBarFixed进行绑定，如果navBarFixed为true时，就应用这个isFixed样式 -->
      <div class="A1">
        <div>
          <img
            src="https://static.shiyanlou.com/frontend/dist/img/9f43b00.svg"
            alt="logo"
            class="logo"
          />
        </div>
      </div>
      <div class="A2">
        <div class="Aa">
          <div class="a1">企业版</div>
          <div>丨</div>
          <div class="a1">学校版</div>
        </div>
        <div class="sign">登录</div>
        <div class="logon">注册</div>
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
    return {
      navBarFixed: "" //将navBarFixed实例初始化
    };
  },
  methods: { //写入 watchScroll 方法。
    watchScroll() {
      var scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
      //  当滚动超过 60 时，实现吸顶效果

      //监听元素到顶部的距离
      //并判断滚动的距离如果大于了元素到顶部的距离时，
      //设置navBarFixed为true,否则就是false
      if (scrollTop > 60) {
        this.navBarFixed = true;
      } else {
        this.navBarFixed = false;
      }
    }
  },
  mounted() {//写入事件监听，监听滚动条。
    window.addEventListener("scroll", this.watchScroll);
  },
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.All {
  display: flex;
  width: 100%;
  height: 55px;
  font-size: 14px;
  position: relative;
  justify-content: center;
  align-items: center;
}
.A1 {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  left: 150px;
}
.A2 {
  width: 210px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  right: 150px;
}
.Aa {
  display: flex;
  justify-content: center;
  align-items: center;
  color: #999;
}
.a1:hover {
  cursor: pointer;
  color: #08bf91;
}
.logo {
  width: 122px;
  height: 50px;
}
.logon {
  width: 56px;
  height: 28px;
  background: #08bf91;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}
.logon:hover {
  cursor: pointer;
}
.logo:hover {
  cursor: pointer;
}
.sign {
  color: #08bf91;
}
.sign:hover {
  cursor: pointer;
  color: rgb(5, 118, 89);
}
// 写一个该元素固定到顶部的样式，isFixed
.navBarWrap {
  position: fixed;
  top: 0;
  z-index: 999;
  background: #fff;
 } 
</style>