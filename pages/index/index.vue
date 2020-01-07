<template>
	<view class="content">
		<!-- banner -->
		<view class="uni-padding-wrap">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper
						class="swiper swiperHeight"
						:indicator-dots="'true'"
						:indicator-active-color="'#fff'"
						:indicator-color="'rgb(255,255,255,.5)'"
						:autoplay="'true'"
						:interval="'2000'"
						:duration="'500'"
					>
						<swiper-item><image src="../../static/img/index/banner.png" mode=""></image></swiper-item>
						<swiper-item><image src="../../static/img/index/banner.png" mode=""></image></swiper-item>
						<swiper-item><image src="../../static/img/index/banner.png" mode=""></image></swiper-item>
					</swiper>
				</view>
			</view>
		</view>
		<!-- 顶部 -->
		<view class="top">
			<view class="city">
				选择城市
			</view>
			<view class="search">
				<input type="text" value="" class="uni-input" placeholder="请输入关键词" />
			</view>
			<view class="scan">
				<text>扫描</text>
				<text>通知</text>
			</view>
		</view>
		<!-- nav -->
		<view class="nav">
			<navigator>
				<text></text>
				<text>停车场</text>
			</navigator>
			<navigator>
				<text></text>
				<text>天气查询</text>
			</navigator>
			<navigator>
				<text></text>
				<text>特色餐厅</text>
			</navigator>
			<navigator>
				<text></text>
				<text>周边景点</text>
			</navigator>
			<navigator>
				<text></text>
				<text>问答</text>
			</navigator>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	onLoad() {},
	methods: {
		
	}
};
</script>

<style>
	.content{
		background-color: #ebedf4;
	}
.swiperHeight {
	height: 184rpx;
}
.top{
	position: absolute;
	display: flex;
	width: 100%;
	top: 0;
	left: 0;
	height: 90rpx;
	align-items: center;
}
.top .city{
	text-align: center;
	font-size: 24rpx;
	flex: 1;
	color: #fff;
}

.top .search{
	flex: 3;
}
.top .search input{
	background-color: #fff;
	border-radius: 12rpx;
	height: 50rpx;
	font-size: 24rpx;
	padding-left: 70rpx;
}
.top .scan{
	width: 150rpx;
	font-size: 5rpx;
}
.nav{
	position: absolute;
	top: 168rpx;
	margin-left: 10rpx;
	display: flex;
	width: 730rpx;
	height: 100rpx;
	align-items: center;
	background-color: #fff;
	border-radius: 10rpx;
	box-shadow: 0px 0px 20rpx #777;
}
.nav navigator{
	flex: 1;
	display: flex;
	align-items: center;
	flex-direction: column;
}
.nav navigator text{
	display: block;
	font-size: 26rpx;
	color: #49494a;
}
.nav navigator text:first-child{
	width: 40rpx;
	height: 40rpx;
	background-image: url(../../static/img/index/bg.png);
	background-size: 156px 236px;
}
.nav navigator:first-child text:first-child{
	background-image: url(../../static/img/index/bg.png);
	background-repeat: 0 0;
	background-size: 156px 236px;
}
.nav navigator:nth-child(2) text:first-child{
	background-position:-125px 0px;
}
.nav navigator:nth-child(3) text:first-child{
	background-position:-63px 0px;
}
.nav navigator:nth-child(4) text:first-child{
	background-position:-96px 0px;
}
.nav navigator:last-child text:first-child{
	background-position: -29px 0px;
}
/* 修改內部样式 */
/deep/ uni-swiper .uni-swiper-dots-horizontal {
	left: 82%;
	bottom: 26rpx;
}
</style>
