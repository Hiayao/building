<template>
  <div>
    <!-- 全部课程导航 -->
    <div class="dev">
      <div v-for="item in course" :key="item.id" class="courseDiv">
        <div class="course">
          <div class="c2">{{item.name}}</div>
          <div class="c1">{{item.tags[0].name}}</div>
          <div class="c1">{{item.tags[1].name}}</div>
        </div>
      </div>
      <div class="c3">经管专区</div>
    </div>
    <!-- 先隐藏鼠标移入后显示的课程分类 -->
    <div class="dev2">
      <div v-for="item in course" :key="item.id">
        <!-- <div v-for="(item1,index) in item.tags" :key="index">{{item1.name}}</div> -->
        <!-- <div v-for="(item2,index) in item.recommend_courses" :key="index">{{item2.name}}</div> -->
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "",
  props: {},
  components: {},
  data() {
    return {
      course: [] //课程分类
    };
  },
  methods: {
    getData() {
      axios
        .get("http://120.78.14.107/api/v2/index/categories")
        .then(res => {
          this.course = res.data;
          console.log(this.course);
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
.dev {
  width: 220px;
  height: 380px;
  background: rgba(0, 0, 0, 0.1);
  position: absolute;
  left: 150px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.courseDiv {
  border-bottom: 1px solid rgba(225, 225, 225, 0.5);
  width: 220px;
  height: 41px;
}
.course {
  font-size: 13px;
  color: white;
  line-height: 41px;
  display: flex;
  &:hover {
    background: white;
    color: black;
  }
}
.c3 {
  height: 16px;
  width: 70px;
  font-size: 10px;
  color: white;
  border: 1px solid white;
  border-radius: 20px 20px 20px 20px;
  margin-top: 12px;
  text-align: center;
  &:hover {
    background: white;
    color: black;
    cursor: pointer;
  }
}
.c1 {
  font-size: 10px;
  margin-left: 8px;
}
.c2 {
  padding-left: 20px;
}
.c1:hover {
  cursor: pointer;
  color: #08bf91;
}
.c2:hover {
  cursor: pointer;
  color: #08bf91;
}
.dev2 {
  background: rgb(139, 210, 212);
  width: 220px;
  height: 380px;
  position: absolute;
  left: 370px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>