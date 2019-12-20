<template>
	<view class="content">
		<view class="logo"><image src="../../static/img/login/JD.png" mode=""></image></view>
		<p class="title">景典账号登录</p>
		<view class="from">
			<view class="uni-form-item uni-column item">
				<input class="uni-input" @input="onGetPhone" v-model="phone" placeholder="请输入手机号" maxlength="11" />
				<text class="warning" v-if="showPhone">请输入正确的手机号码</text>
			</view>
			<view class="uni-form-item uni-column item"><input class="uni-input" v-model="password" maxlength="10" placeholder="请输入密码" /></view>
			<view class="uni-form-item uni-column item">
				<navigator url="../register/index">注册</navigator>
				<text>找回密码</text>
			</view>
			<button @click="onSubmit">登录</button>
		</view>
		<view class="agree">
			<text>登录即代表您同意我们的</text>
			<text>《服务协议》</text>
			<text>和</text>
			<text>《隐私政策》</text>
		</view>
		<mpopup ref="mpopup" :isdistance="true"></mpopup>
	</view>
</template>

<script>
	import mpopup from '../../components/xuan-popup/xuan-popup.vue'
export default {
	components:{
		mpopup
	},
	data() {
		return {
			timer: null,
			phone: '',
			password: '',
			code: '',
			showPhone: false
		};
	},
	methods: {
		// 验证手机号码
		onGetPhone() {
			if (this.timer) {
				clearTimeout(this.timer);
			}
			this.timer = setTimeout(() => {
				const reg = new RegExp(/^(13[0-9]|14[5|7]|15[0|1|2|3|4|5|6|7|8|9]|18[0|1|2|3|5|6|7|8|9])\d{8}$/);
				if (!reg.test(this.phone)) {
					this.showPhone = true;
				} else {
					this.showPhone = false;
				}
			}, 300);
		},
		// 登录
		onSubmit() {
			const reg = new RegExp(/^(13[0-9]|14[5|7]|15[0|1|2|3|4|5|6|7|8|9]|18[0|1|2|3|5|6|7|8|9])\d{8}$/);

			if (reg.test(this.phone) && this.phone == '15976593304') {
				if (this.password && this.password == '888888') {
					uni.switchTab({
						url: '/pages/index/index'
					});
				} else {
					this.$refs.mpopup.open({
						type: 'err',
						content: '请输入密码',
						timeout: 1000
					});
				}
			} else {
				this.$refs.mpopup.open({
					type: 'err',
					content: '请输入正确的手机号码',
					timeout: 1000
				});
			}
		}
	},
	mounted() {}
};
</script>

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
.content .from {
	margin-top: 10rpx;
	padding: 0 40rpx;
}
.content .from .item {
	height: 106rpx;
	border-bottom: 1rpx solid #bcbcbc;
	display: flex;
	align-items: center;
	justify-content: space-between;
}
.content .from .item:nth-child(3) {
	border: none;
	font-size: 26rpx;
	color: #666666;
	font-weight: 600;
	justify-content: space-between;
}
.content button {
	margin-top: 20rpx;
	background-color: #2f56e4;
	line-height: 70rpx;
	color: #fff;
	font-size: 30rpx;
}
.content .agree {
	position: fixed;
	bottom: 68rpx;
	width: 100%;
	text-align: center;
	font-size: 24rpx;
}
.content .agree text:nth-child(2n) {
	color: #4469f2;
}
.content .from .item .warning {
	font-size: 12rpx;
	color: #f00;
	text-align: right;
}
</style>
