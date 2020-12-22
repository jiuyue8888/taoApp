<template>
	<div :class="pc?'mian pc':'mian'" :style="pc?`width:${wid-50}px;height:100vh`:''">
		<div class="content">
		<div class="icons">
			<svg-icon icon-class="tianmao" :size="pc?size[0][0]:size[0][0]" class="tianmao animated fadeInUp1 infinite"/>
			<svg-icon icon-class="taobao" :size="pc?size[1][0]:size[1][0]" class="taobao animated fadeInUp1 infinite"/>
			<svg-icon icon-class="pingdd" :size="pc?size[2][0]:size[2][0]" class="pingdd animated fadeInUp1 infinite"/>
			<svg-icon icon-class="taopp" :size="pc?size[3][0]:size[3][0]" class="taopp animated fadeInUp2 infinite"/>
			<svg-icon icon-class="icon37" :size="pc?size[4][0]:size[4][0]" class="icon37 animated fadeInUp1 infinite"/>
			<svg-icon icon-class="icon34" :size="pc?size[5][0]:size[5][0]" class="icon34 animated fadeInUp2 infinite"/>
			<svg-icon icon-class="icon35" :size="pc?size[6][0]:size[6][0]" class="icon35 animated fadeInUp1 infinite"/>
			<svg-icon icon-class="icon36" :size="pc?size[7][0]:size[7][0]" class="icon36 animated fadeInUp2 infinite"/>
			<svg-icon icon-class="icon33" :size="pc?size[8][0]:size[8][0]" class="icon33 animated fadeInUp2 infinite"/>
		</div>
		<div class="people animated fadeInUp infinite">
			<img v-if="pcc" src="../../assets/people.png"/>
			<svg-icon v-else icon-class="people" :size="pc?size[9][0]:size[9][0]"/>
		</div>
		<div class="map animated rotateIn infinite">
			<img v-if="pcc" src="../../assets/map.png"/>
			<svg-icon v-else icon-class="map" :size="pc?size[10][1]:size[10][0]"/>
		</div>
		<div class="mask">
			<img v-if="pcc" src="../../assets/mask.png"/>
			<svg-icon v-else icon-class="zhezhao" :size="pc?size[11][1]:size[11][0]"/>
		</div>
		</div>
		<div class="float" v-show="!pc">
			<div class="left">
				<svg-icon icon-class="icon32" :size="pc?size[12][1]:size[12][0]" class="icon32"/>
				<div>
					<h3>自购省钱 分享赚钱</h3>
					<p>买撒都优惠 买撒都返利</p>
				</div>
			</div>
			<div class="right">下载APP</div>
		</div>
		<div class="rf" v-show="pc">
			<div class="ewm">
				<p>官方邀请码：999992</p>
				<img src="../../assets/timg.jpeg" />
				<h5>手机扫一扫</h5>
			</div>
			<div class="nav">
				<span><svg-icon icon-class="video" size="33px,33px"/></span>
				<span><svg-icon icon-class="qq" size="33px,33px"/></span>
				<span><svg-icon icon-class="wx" size="33px,33px"/></span>
				
				<span><svg-icon icon-class="tel" size="33px,33px"/></span>
				<span><svg-icon icon-class="mobile" size="33px,33px"/></span>
			</div>
		</div>
		<div class="footer" v-show="pc">&#1692020 Taozi 苏ICP备20047418号-1 苏公网安备 0000000000号</div>
		
	</div>
</template>

<script>
	import 'amfe-flexible';
	export default {
		name: 'main',
		data() {
			return {
				pcc:true,
				pc:false,//window.innerWidth>450,
				screenWidth: '',
				        screenHeight: '',
						wid:'',
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
					['375px,375px','450px,3.75rem'],
					['375px,231px','600px,231px'],
					['44px,44px','0.44rem,0.44rem'],
				]
			}
		},
		created(){
			
			
		},
		watch:{
		    	//窗口宽度变化
		      	screenWidth (val) {
		          console.log(val)
				  this.pc=val>450
		      	},
		      	//窗口高度变化
		      	screenHeight (val) {
		          console.log(val)
				  this.wid = 375*val/592
		      }    
		  	},
		mounted() {
		      this.screenWidth = document.body.clientWidth;
		      this.screenHeight = document.body.clientHeight;
		      window.onresize = () => {
		        return (() => {
				  this.pc=document.body.clientWidth>750
		          this.screenWidth = document.body.clientWidth;
		          this.screenHeight = document.body.clientHeight;
				  this.wid = 375*document.body.clientHeight/592
		        })();
		      };
		    },
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.rf{
		position: fixed;
		right: 120px;
		bottom: 150px;
		padding-left: 180px;
		
	}
	.nav{
		width: 60px;
		background: #ffffff;
		border-radius: 6px;
		box-shadow: 0px 9px 24px 0px rgba(124,124,124,0.22); 
	}
	.ewm{
		position: absolute;
		left: 5px;
		bottom: 0;
		width: 155px;
		box-sizing: border-box;
		padding: 18px 10px;
		border-radius: 10px;
		font-size: 13px;
		
		text-align: center;
		background: #ffffff;
		border-radius: 6px 6px 0px 0px 0px 6px 6px;
		box-shadow: 0px 9px 24px 0px rgba(124,124,124,0.22); 
	}
	.ewm::after{
		position: absolute;
		right: -8px;
		bottom: 20px;
		content: '';
		border-top:8px transparent solid;
		border-bottom:8px transparent solid;
		border-left:8px #fff solid;
	}
	.ewm h5{
		font-size: 16px;
		padding-top: 10px;
	}
	.ewm p{
		padding-bottom: 10px;
	}
	.nav span{
		display: block;
		width: 60px;
		height: 60px;
		box-sizing: border-box;
		padding: 14px;
		border-bottom: 1px solid rgba(232,232,232,0.22);
	}
	.mian {
		position: relative;
		width: 100%;
		min-height: 100vh;
		max-width: 450px;
		overflow: hidden;
		background: url(../../assets/bg.jpg) no-repeat 0 0 #5608a9;
		background-size: 100%;
	}
	.content{
		position: relative;
		width: 100%;
		height: calc(100vh - 76px);
		overflow: hidden;
		
	}
	.footer{
		position: fixed;
		    width: 100%;
		    left: 0;
		    text-align: center;
		    font-size: 12px;
		    height: 50px;
		    line-height: 50px;
		    background-color: #fff;
		    color: #848484;
		    border-top: 1px solid rgba(232,232,232,0.67);
	}
	.left{
		display: flex;
		align-items: center;
	}
	.left h3{
		
		font-size: 16px;
		font-family: PingFangSC, PingFangSC-Regular;
		font-weight: 400;
		text-align: left;
		color: #ffffff;
		line-height: 17px;
		letter-spacing: 2px;
	}
	.left p{
		transform-origin: 0 100%;
		transform: scale(0.5);
		font-size: 16px;
		font-family: PingFangSC, PingFangSC-Regular;
		font-weight: 400;
		text-align: left;
		color: #ffffff;
		line-height: 17px;
		letter-spacing: 2px;
	}
	.right{
		width: 76px;
		height: 32px;
		text-align: center;
		line-height: 32px;
		background: #fb5753;
		border-radius: 16px;
		font-size: 12px;
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
		height: 76px;
		box-sizing: border-box;
		padding: 16px 20px;
		background: #000;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}
	.people{
		position: absolute;
		left: 0;
		top: 1.86rem;
		z-index: 5;
		animation-duration: 3s;
	}
	.map{
		position: absolute;
		left: 0;
		bottom: -4rem;
		z-index: 1;
		animation-duration: 15s;
	}
	.mask{
		position: absolute;
		left: 0;
		bottom: 0;
		z-index: 6;
		width: 100%;
	}
	.tianmao{
		position: absolute;
		left: 1rem;
		top: 2.46rem;
		z-index: 2;
		animation-duration: 3s;
	}
	.taobao{
		position: absolute;
		left: 1.04rem;
		top: 8.22rem;
		z-index: 2;
		animation-duration: 4s;
	}
	.pingdd{
		position: absolute;
		left: 6.22rem;
		top: 4.96rem;
		z-index: 2;
		animation-duration: 2s;
	}
	.taopp{
		position: absolute;
		left: 4.40rem;
		top: 3.62rem;
		z-index: 2;
		animation-duration: 2.5s;
	}
	.icon33{
		position: absolute;
		left: 5.38rem;
		top: 2.46rem;
		z-index: 2;
		animation-duration: 3s;
	}
	.icon34{
		position: absolute;
		left: 0.12rem;
		top: 9.78rem;
		z-index: 2;
		animation-duration: 4s;
	}
	.icon35{
		position: absolute;
		left: 1.04rem;
		top: 10.18rem;
		z-index: 2;
		animation-duration: 2s;
	}
	.icon36{
		position: absolute;
		left: 6.70rem;
		top: 10.32rem;
		z-index: 2;
		animation-duration: 3s;
	}
	.icon37{
		position: absolute;
		left: 5.56rem;
		top: 9.78rem;
		z-index: 2;
		animation-duration: 2s;
	}
	.pc{
		
		margin: 0 auto;
	}
	.pc .content{
		position: relative;
		width: 100%;
		height: calc(100% - 50px);
		overflow: hidden;
		
	}
	.pc .float{
		display: none;

	}
	.pc .people{
		top: 186px;
	}
	.pc .map{	
		bottom: -250px;
	}
	
	.pc .tianmao{
		position: absolute;
		left: 50px;
		top: 123px;
		z-index: 2;
	}
	.pc .taobao{
		position: absolute;
		left: 52px;
		top: 411px;
		z-index: 2;
	}
	.pc .pingdd{
		position: absolute;
		left: 311px;
		top: 248px;
		z-index: 2;
	}
	.pc .taopp{
		position: absolute;
		left: 22px;
		top: 181px;
		z-index: 2;
	}
	.pc .icon33{
		position: absolute;
		left: 269px;
		top: 123px;
		z-index: 2;
	}
	.pc .icon34{
		position: absolute;
		left: 6px;
		top: 489px;
		z-index: 2;
	}
	.pc .icon35{
		position: absolute;
		left: 52px;
		top: 509px;
		z-index: 2;
	}
	.pc .icon36{
		position: absolute;
		left: 335px;
		top: 516px;
		z-index: 2;
	}
	.pc .icon37{
		position: absolute;
		left: 278px;
		top: 489px;
		z-index: 2;
	}
</style>
