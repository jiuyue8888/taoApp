<template>
	<div :class="pc?'mian pc':'mian'">
		<div class="content">
		<div class="icons">
			<svg-icon icon-class="tianmao" :size="pc?size[0][1]:size[0][0]" class="tianmao animated fadeInUp1 infinite"/>
			<svg-icon icon-class="taobao" :size="pc?size[1][1]:size[1][0]" class="taobao animated fadeInUp1 infinite"/>
			<svg-icon icon-class="pingdd" :size="pc?size[2][1]:size[2][0]" class="pingdd animated fadeInUp1 infinite"/>
			<svg-icon icon-class="taopp" :size="pc?size[3][1]:size[3][0]" class="taopp animated fadeInUp2 infinite"/>
			<svg-icon icon-class="icon37" :size="pc?size[4][1]:size[4][0]" class="icon37 animated fadeInUp1 infinite"/>
			<svg-icon icon-class="icon34" :size="pc?size[5][1]:size[5][0]" class="icon34 animated fadeInUp2 infinite"/>
			<svg-icon icon-class="icon35" :size="pc?size[6][1]:size[6][0]" class="icon35 animated fadeInUp1 infinite"/>
			<svg-icon icon-class="icon36" :size="pc?size[7][1]:size[7][0]" class="icon36 animated fadeInUp2 infinite"/>
			<svg-icon icon-class="icon33" :size="pc?size[8][1]:size[8][0]" class="icon33 animated fadeInUp2 infinite"/>
		</div>
		<div class="people animated fadeInUp infinite">
			<svg-icon icon-class="people" :size="pc?size[9][1]:size[9][0]"/>
		</div>
		<div class="map animated rotateIn infinite">
			<svg-icon icon-class="map" :size="pc?size[10][1]:size[10][0]"/>
		</div>
		<div class="mask">
			<svg-icon icon-class="zhezhao" :size="pc?size[11][1]:size[11][0]"/>
		</div>
		</div>
		<div class="footer" v-if="pc">&#1692020 Taozi 苏ICP备20047418号-1 苏公网安备 0000000000号</div>
		<div class="float" v-else>
			<div class="left">
				<svg-icon icon-class="icon32" :size="pc?size[12][1]:size[12][0]" class="icon32"/>
				<div>
					<h3>自购省钱 分享赚钱</h3>
					<p>买撒都优惠 买撒都返利</p>
				</div>
			</div>
			<div class="right">下载APP</div>
		</div>
		
	</div>
</template>

<script>
	export default {
		name: 'main',
		data() {
			return {
				pc:window.innerWidth>750,
				size:[
					['56px,69px','0.56rem,0.69rem'],
					['54px,58px','0.54rem,0.58rem'],
					['35px,35px','0.35rem,0.35rem'],
					['38px,43px','0.38rem,0.43rem'],
					['20px,20px','0.2rem,0.20rem'],
					['24px,25px','0.24rem,0.25rem'],
					['32px,26px','0.32rem,0.26rem'],
					['32px,26px','0.32rem,0.26rem'],
					['35px,32px','0.35rem,0.32rem'],
					['375px,483px','3.75rem,4.83rem'],
					['375px,375px','3.75rem,3.75rem'],
					['375px,231px','3.75rem,2.31rem'],
					['44px,44px','0.44rem,0.44rem'],
				]
			}
		},
		created(){
			
			
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.mian {
		position: relative;
		width: 750px;
		min-height: 100vh;
		
		overflow: hidden;
		background: url(../../assets/bg.jpg) no-repeat 0 0 #5608a9;
		background-size: 100%;
	}
	.content{
		position: relative;
		width: 100%;
		height: calc(100vh - 152px);
		overflow: hidden;
		
	}
	.footer{
		position: relative;
		width: 100%;
		text-align: center;
		font-size: 0.12rem;
		height: 0.5rem;
		line-height: 0.5rem;
		background-color: #fff;
		color: #848484;
	}
	.left{
		display: flex;
		align-items: center;
	}
	.left h3{
		
		font-size: 32px;
		font-family: PingFangSC, PingFangSC-Regular;
		font-weight: 400;
		text-align: left;
		color: #ffffff;
		line-height: 34px;
		letter-spacing: 2px;
	}
	.left p{
		transform-origin: 0 100%;
		transform: scale(0.5);
		font-size: 32px;
		font-family: PingFangSC, PingFangSC-Regular;
		font-weight: 400;
		text-align: left;
		color: #ffffff;
		line-height: 34px;
		letter-spacing: 2px;
	}
	.right{
		width: 152px;
		height: 64px;
		text-align: center;
		line-height: 64px;
		background: #fb5753;
		border-radius: 32px;
		font-size: 24px;
		font-family: PingFang, PingFang-SC;
		font-weight: SC;
		
		color: #ffffff;
		
		letter-spacing: 2px;
	}
	.icon32{
		margin-right: 14px;
	}
	.float{
		position: relative;
		z-index: 3;
		width: 100%;
		height: 152px;
		box-sizing: border-box;
		padding: 32px 40px;
		background: #000;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.people{
		position: absolute;
		left: 0;
		top: 186px;
		z-index: 5;
		animation-duration: 3s;
	}
	.map{
		position: absolute;
		left: 0;
		bottom: -400px;
		z-index: 1;
		animation-duration: 15s;
	}
	.mask{
		position: absolute;
		left: 0;
		bottom: 0;
		z-index: 6;
	}
	.tianmao{
		position: absolute;
		left: 100px;
		top: 246px;
		z-index: 2;
		animation-duration: 3s;
	}
	.taobao{
		position: absolute;
		left: 104px;
		top: 822px;
		z-index: 2;
		animation-duration: 4s;
	}
	.pingdd{
		position: absolute;
		left: 622px;
		top: 496px;
		z-index: 2;
		animation-duration: 2s;
	}
	.taopp{
		position: absolute;
		left: 440px;
		top: 362px;
		z-index: 2;
		animation-duration: 2.5s;
	}
	.icon33{
		position: absolute;
		left: 538px;
		top: 246px;
		z-index: 2;
		animation-duration: 3s;
	}
	.icon34{
		position: absolute;
		left: 12px;
		top: 978px;
		z-index: 2;
		animation-duration: 4s;
	}
	.icon35{
		position: absolute;
		left: 104px;
		top: 1018px;
		z-index: 2;
		animation-duration: 2s;
	}
	.icon36{
		position: absolute;
		left: 670px;
		top: 1032px;
		z-index: 2;
		animation-duration: 3s;
	}
	.icon37{
		position: absolute;
		left: 556px;
		top: 978px;
		z-index: 2;
		animation-duration: 2s;
	}
	.pc{
		width: 3.75rem;
		margin: 0 auto;
	}
	.pc .content{
		position: relative;
		width: 100%;
		height: calc(100vh - 0.5rem);
		overflow: hidden;
		
	}
	.pc .float{
		display: none;

	}
	.pc .people{
		top: 0.93rem;
	}
	.pc .map{	
		bottom: -2rem;
	}
	
	.pc .tianmao{
		position: absolute;
		left: 0.5rem;
		top: 1.23rem;
		z-index: 2;
	}
	.pc .taobao{
		position: absolute;
		left: 0.52rem;
		top: 4.11rem;
		z-index: 2;
	}
	.pc .pingdd{
		position: absolute;
		left: 3.11rem;
		top: 2.48rem;
		z-index: 2;
	}
	.pc .taopp{
		position: absolute;
		left: 2.2rem;
		top: 1.81rem;
		z-index: 2;
	}
	.pc .icon33{
		position: absolute;
		left: 2.69rem;
		top: 1.23rem;
		z-index: 2;
	}
	.pc .icon34{
		position: absolute;
		left: 0.06rem;
		top: 4.89rem;
		z-index: 2;
	}
	.pc .icon35{
		position: absolute;
		left: 0.52rem;
		top: 5.09rem;
		z-index: 2;
	}
	.pc .icon36{
		position: absolute;
		left: 3.35rem;
		top: 5.16rem;
		z-index: 2;
	}
	.pc .icon37{
		position: absolute;
		left: 2.78rem;
		top: 4.89rem;
		z-index: 2;
	}
</style>
