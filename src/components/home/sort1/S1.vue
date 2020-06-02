<template>
  <div>
    <div class="all">
      <div class="s1">
        <div>楼+ 实战课程</div>
        <div>丨</div>
        <div class="w1">定期开班，导师助教全程辅导，最快最优成长</div>
      </div>
      <div class="s2">更多></div>
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
.all {
  width: 1240px;
  height: 60px;
  background:#f9f9f9;
  display: flex;
  align-items: center;
  position: relative;
}
.s1 {
  padding-left: 150px;
  display: flex;
  font-size: 18px;
  &:hover {
    cursor: pointer;
  }
}
.w1 {
  font-size: 12px;
  padding-top: 6px;
  color: rgb(73, 68, 68);
}
.s2 {
  font-size: 12px;
  width: 40px;
  line-height: 60px;
  position: absolute;
  right: 150px;
  color: rgb(73, 68, 68);
  &:hover {
    cursor: pointer;
  }
}
</style>