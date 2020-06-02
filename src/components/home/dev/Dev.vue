<template>
  <div>
    <div class="All">
      <D1></D1>
      <D2></D2>
    </div>
  </div>
</template>

<script>
import D1 from "../dev/D1";
import D2 from "../dev/D2";
export default {
  name: "",
  props: {},
  components: {
    D1,
    D2
  },
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
    width: 1240px;
    height: 380px;
    background: skyblue;
    display: flex;
    position: relative;
}
</style>