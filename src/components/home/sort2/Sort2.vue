<template>
  <div>
    <div class="All">
      <S1></S1>
      <S2></S2>
    </div>
  </div>
</template>

<script>
import S1 from "../sort2/S1";
import S2 from "../sort2/S2";
export default {
  name: "",
  props: {},
  components: {
    S1,
    S2
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
  height: 390px;
  width: 1240px;
  background: yellowgreen;
  margin-top: 10px;
}
</style>