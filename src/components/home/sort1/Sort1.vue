<template>
 <div>
<div class="All">
    <S1></S1>
    <S2></S2>
    
</div>
 </div>
</template>

<script>
import S1 from '../sort1/S1'
import S2 from '../sort1/S2'
 export default {
   name: '',
   props: {
   },
   components: {
S1,S2
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
.All{
    width: 1240px;
    height: 200px;
    background: chartreuse;
}
</style>