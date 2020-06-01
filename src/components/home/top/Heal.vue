<template>
  <div>
    <div class="box" v-if="todos.length > 0">
      <div v-for="(item,index) in todos" :key="index" class="box1">
        <div @mouseleave="leave(item)" @mouseenter="enter(item)" class="mouse">
          <div>
            <input type="checkbox" v-model="item.complete"/>
          </div>
          <div class="word">{{item.title}}</div>
          <div>
            <button class="del" v-if="item.hover" @click="del(item,index)">删除</button>
          </div>
        </div>
      </div>
    </div>
    <div v-else>暂无任务</div>
  </div>
</template> 

<script>
export default {
  name: "",
  props: {
    todos: {
      type: Array,
      
    },
    
  },
  components: {},
  data() {
    return {
      
    };
  },
  methods: {
    enter(item) {
      item.hover = true;
    },
    leave(item) {
      item.hover = false;
    },
    del(item,index){
      this.$emit('del',index)
    }
  },
  mounted() {
    this.todos.map(item => {
      //给对象添加原本没有的属性，用this.$set(),
      //第一个为对象，第二个为键（引号引起来），第三个为值
      this.$set(item, "hover", false);
    });
  },
  watch: {},
  computed: {}
};
</script>

<style scoped lang='scss'>
.box {
  margin-top: 20px;
  border: 1px solid #999;
  width: 380px;
  position: relative;
}
.del {
  
  background: red;
  position: absolute;
  right: 0px;
  
}
.box1 {
  display: flex;
  &:hover {
    background: #999;
  }
}
.mouse {
  display: flex;
}
.word {
  width: 380px;
}
</style>