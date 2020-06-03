<template>
 <div>
	 <div class="All">
		 <T1></T1>
		 <T2></T2>
		 <T3></T3>
	 </div>

 </div>
</template>

<script>
import T1 from '../top/T1'
import T2 from '../top/T2'
import T3 from '../top/T3'
 export default {
	 name: '',
	 props: {
	 },
	 components: {
T1,T2,T3
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
.All {
	width: 1240px;
	height: 105px;
	margin: 0px;
	background: #F9F9F9;
}
</style>