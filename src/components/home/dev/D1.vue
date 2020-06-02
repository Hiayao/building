<template>
 <div>
<div class="all">
    <div class="left"></div>
    <div class="center"></div>
    <div class="right"></div>
</div>
 </div>
</template>

<script>
 export default {
   name: '',
   props: {
   },
   components: {

   },
   data () {
     return {

     }
   },
   methods: {

   },
   mounted() {

   },
   watch: {

   },
   computed: {

   }
 }
</script>

<style scoped lang='scss'>
.all {
    width: 1240px;
    height: 380px;
    display: flex;
}
.left {
    width: 370px;
    height: 380px;
    background: pink;
}
.center {
    width: 720px;
    height: 380px;
}
.right {
    width: 150px;
    height: 380px;
    background: pink;
}
</style>