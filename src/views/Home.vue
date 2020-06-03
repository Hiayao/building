<template>
  <div>
    <Top></Top>
    <Dev></Dev>
    <Sort1></Sort1>
    <Sort2></Sort2>
  </div>
</template>

<script>
import Top from "../components/home/top/Top";
import Dev from "../components/home/dev/Dev";
import Sort1 from "../components/home/sort1/Sort1";
import Sort2 from "../components/home/sort2/Sort2";
export default {
  name: "",
  props: {},
  components: {
    Top,
    Dev,
    Sort1,
    Sort2
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
</style>