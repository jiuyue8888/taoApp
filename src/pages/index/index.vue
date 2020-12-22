<template>
	<div class="mian">
		
		<div class="icons">
			<svg-icon icon-class="tianmao" size="56px,69px" class="tianmao"/>
			<svg-icon icon-class="taobao" size="54px,58px" class="taobao"/>
			<svg-icon icon-class="pingdd" size="35px,35px" class="pingdd"/>
			<svg-icon icon-class="taopp" size="38px,43px" class="taopp"/>
			<svg-icon icon-class="icon37" size="20px,20px" class="icon37"/>
			<svg-icon icon-class="icon34" size="24px,25px" class="icon34"/>
			<svg-icon icon-class="icon35" size="32px,26px" class="icon34"/>
			<svg-icon icon-class="icon33" size="35px,32px" class="icon34"/>
		</div>
		<div class="people animated infinite">
			<svg-icon icon-class="people" size="375px,483px"/>
		</div>
		<div class="map">
			<svg-icon icon-class="map" size="375px,351px"/>
		</div>
		<div class="mask">
			<svg-icon icon-class="zhezhao" size="375px,231px"/>
		</div>
		<div class="float"></div>
	</div>
</template>

<script>
	export default {
		name: 'main',
		data() {
			return {
				
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.mian {
		position: relative;
		width: 750px;
		height: 100vh;
		overflow: hidden;
		background: url(../../assets/bg.jpg) no-repeat 0 0 #5608a9;
		background-size: 100%;
	}
	.people{
		position: absolute;
		left: 0;
		top: 186px;
		z-index: 5;
	}
	.map{
		position: absolute;
		left: 0;
		bottom: -900px;
		z-index: 1;
	}
	.mask{
		position: absolute;
		left: 0;
		bottom: 0;
		z-index: 6;
	}
	.tianmao{
		position: absolute;
		left: 50px;
		top: 123px;
		z-index: 2;
	}
	
</style>
