<template>
  <div>
    <div class="All">
      <div class="A1">
        <div>
          <img
            src="https://static.shiyanlou.com/frontend/dist/img/9f43b00.svg"
            alt="logo"
            class="logo"
          />
        </div>
        <div>做实验，学编程</div>
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
	color:#08BF91 ;
}
.logo {
  width: 122px;
  height: 50px;
}
.logon {
	width: 56px;
	height: 28px;
	background: #08BF91;
	display: flex;
  justify-content: center;
  align-items: center;
	color: white;
}
.logon:hover{
	cursor: pointer;
}
.logo:hover{
	cursor: pointer;
}
.sign {
	color: #08BF91;
}
.sign:hover{
	cursor: pointer;
	color: rgb(5,118,89);
	} 
</style>