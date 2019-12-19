<template>
	<view class="content">
		<view class="from">
			<form @submit="formSubmit">
				<view class="uni-form-item uni-column item"><input class="uni-input" placeholder="请输入手机号码" /></view>
				<view class="uni-form-item uni-column item"><input class="uni-input" placeholder="请输入密码" /></view>
				<view class="uni-form-item uni-column item">
					<input class="uni-input" placeholder="请输入短信验证码" />
					<text class="code">获取验证码</text>
				</view>
				<view class="uni-form-item uni-column item item2">
					<checkbox-group @change="checkboxChange">
						<label>
							<checkbox value="1" :checked="checked"></checkbox>
							已阅读并同意<text class="blue">用户协议</text>和<text class="blue">隐私协议</text>
						</label>
					</checkbox-group>
				</view>
				<button type="primary" form-type="submit">注册</button>
			</form>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return{
			checked: false
		}
	},
	methods: {
		checkboxChange(e) {}
	}
};
</script>

<style>
.content {
	padding: 0 40rpx;
}
.content .from {
	margin-top: 160rpx;
}
.content .from form .item {
	position: relative;
	display: flex;
	height: 106rpx;
	align-items: center;
	border-bottom: 1rpx solid #d6d6d6;
}
.content .from form .item2 {
	margin-top: 60rpx;
	border: none;
}
.content form .item .code {
	position: absolute;
	top: 50%;
	right: 0;
	transform: translate(0, -50%);
	color: #666666;
	font-size: 22rpx;
}
.content .from form .item2 label{
	font-size: 24rpx;
}
/deep/ uni-checkbox .uni-checkbox-input{
	width: 28rpx !important;
	height: 28rpx !important;
	margin-right: 20rpx;
}
.blue{
	color: #007AFF;
}
.content .from form button{
	background-color: #2f56e4;
	font-size: 30rpx;
	height: 70rpx;
	line-height: 70rpx;
}
</style>
