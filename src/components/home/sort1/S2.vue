<template>
  <div>
    <div class="all">
      <div class="picAll">
        <div class="picture" v-for="(item,index) in list.slice(0,4)" :key="index">
          <div style="height: 70px">
            <img :src="item.picture_url" alt class="pic1" />
          </div>
          <div class="pic">
            <div class="pic2">{{item.title}}</div>
            <div class="pic3">最近班次：{{item.open_time}}</div>
          </div>
        </div>
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
      list: []
    };
  },
  methods: {
    getData() {
      axios
        .get("http://120.78.14.107/api/v2/index/louplus")
        .then(res => {
          this.list = res.data;
          console.log(this.list);
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
  height: 140px;
  position: relative;
  background: #f9f9f9;
}
.picAll {
  width: 940px;
  height: 140px;
  display: flex;
  position: absolute;
  left: 150px;
  justify-content: space-between;
}
.picture {
  width: 200px;
  height: 143px;
  border: 0.5px solid #f9f9f9;
  border-radius: 8px 8px 8px 8px;
  &:hover{
      box-shadow: 0px 5px 10px 0px rgb(190, 188, 188);
      cursor: pointer;
  }
}
.pic1 {
  width: 199px;
  height: 69px;
  border: 0.5px solid #f9f9f9;
  border-radius: 8px 8px 0px 0px;
}
.pic2 {
  font-size: 14px;
}
.pic3 {
  font-size: 13px;
  color: #999;
}
.pic {
  height: 70px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: white;
  padding-left: 10px;
  border: 0.5px solid #f9f9f9;
  border-radius:  0px 0px 8px 8px;
}
</style>