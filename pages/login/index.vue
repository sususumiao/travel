<template>
	<view class="content">
		<view class="logo"><image src="../../static/img/login/JD.png" mode=""></image></view>
		<p class="title">景典账号登录</p>
		<view class="from">
			<view class="uni-form-item uni-column item">
				<input class="uni-input" @input="onKeyInput" placeholder="手机号/用户名/邮箱" />
			</view>
			<view class="uni-form-item uni-column item">
				<input class="uni-input" @input="onKeyInput" placeholder="请输入密码" />
			</view>
			<view class="uni-form-item uni-column item">
				<navigator url="../register/index">注册</navigator>
				<text>找回密码</text>
			</view>
			<button>登录</button>
		</view>
		<view class="agree">
			<text>登录即代表您同意我们的</text>
			<text>《服务协议》</text>
			<text>和</text>
			<text>《隐私政策》</text>
		</view>
	</view>
</template>

<script></script>

<style>
.content {
	padding-top: 60rpx;
}
.content .logo {
	margin: 0 auto;
	width: 188rpx;
	height: 188rpx;
}
.content .title {
	margin-top: 30rpx;
	font-size: 32rpx;
	text-align: center;
}
.content .from{
	margin-top: 10rpx;
	padding: 0 40rpx;
}
.content .from .item{
	height: 106rpx;
	border-bottom: 1rpx solid #bcbcbc;
	display: flex;
	align-items: center;
}
.content .from .item:nth-child(3){
	border: none;
	font-size: 26rpx;
	color: #666666;
	font-weight: 600;
	justify-content: space-between;
}
.content button{
	margin-top: 20rpx;
	background-color: #805ad7;
	line-height: 70rpx;
	color: #fff;
	font-size: 30rpx;
}
.content .agree{
	position: fixed;
	bottom: 68rpx;
	width: 100%;
	text-align: center;
	font-size: 24rpx;
}
.content .agree text:nth-child(2n){
	color: #4469f2;
}
</style>
