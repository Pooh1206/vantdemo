<template>
	<view class="cash">
		<view class="cash-top">
			<view class="leiji">可提现金额</view>
			<text class="num" style="font-weight: bold;font-size: 24px;color: #FFFFFF;margin-bottom: 10px">{{money}} 元</text>
			<view style="margin-top: 8px;font-size: 10px;color: #FFFFFF">（可提现金额=已结算订单佣金+邀好友结算佣金）</view>
		</view>
		<view style="padding: 16px;border-radius: 8px">
			<view style="font-size: 14px;color: grey;margin-bottom: 10px">累计提现金额</view>
			<text class="num" style="font-size: 18px;color: #e10a07;margin-bottom: 10px">{{totalMoney}} 元</text>
			<view style="margin-top: 8px;font-size: 10px;color: #999999">（累计提现金额=所有已提现金额总和）</view>
		</view>

		<view style="text-align: center;margin-top: 32px;width: 100%;padding-bottom: 32px">
			<view @click="getOut" v-if="money!=='0'" style="margin-left: 40px;margin-right:40px;font-size: 18px;background: #e10a07;color: white;border-radius: 10px;height: 40px;line-height: 40px">
				提现
			</view>
			<view v-else style="margin-left: 40px;margin-right:40px;font-size: 18px;background: gainsboro;color: white;border-radius: 10px;height: 40px;line-height: 40px">
				暂无可提现金额
			</view>
		</view>
		<view style="display: flex">
			<view style="color: grey;width: 50%;padding-bottom: 30px" @click="goZhifuBao">提现账号</view>
			<view style="color: grey;width: 50%;padding-bottom: 30px" @click="list">提现记录</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				money: '0.00',
				zhifubao: '',
				totalMoney: '0.00',
				zhifubaoName: '',
			}
		},
		onShow: function(e) {
			this.getMoney();
		},

		methods: {
			list() {
				uni.navigateTo({
					url: '/pages/member/cashList'
				})
			},
			goZhifuBao() {
				uni.navigateTo({
					url: "/pages/member"
				})
			},
			getMoney() {
				let that = this;
				let token = this.$queue.getData("token");
				let userId = this.$queue.getData("userId");
				if (token) {
					//this.$queue.showLoading("加载中...");
					//可以提现金额查询预估收入查询
					this.$Request.getT("/cash/money/" + userId).then(res => {
						if (res.status === 0 && res.data) {
							that.money = res.data;
						} else if (res.status === -102) {
							this.$queue.showToast(res.msg);
							this.$queue.logout();
							uni.navigateTo({
								url: '/pages/login'
							})
						} else {
							that.money = '0.00';
							//this.$queue.showToast(res.msg);
						}
					});
					this.$Request.getT("/cash/userinfo/" + userId).then(res => {
						if (res.status === 0 && res.data) {
							that.zhifubao = res.data.zhifubao;
							that.zhifubaoName = res.data.zhifubaoName;
						}
						uni.hideLoading();
					});
					//总的提现记录
					this.$Request.getT("/cash/countByRelationId/" + this.$queue.getData("relation_id")).then(res => {
						if (res.status === 0 && res.data) {
							that.totalMoney = parseFloat(res.data).toFixed(2);
						} else {
							that.totalMoney = '0.00';
						}
					});
				}

			},
			getOut() {
				let that = this;
				let token = this.$queue.getData("token");
				let userId = this.$queue.getData("userId");
				if (token) {
					if (that.zhifubao && that.zhifubaoName) {
						if (parseFloat(this.money).toFixed(1) >= 10) {
							uni.showModal({
								title: "提现申请提示",
								content: '请仔细确认收款人信息\n\n姓名:' + that.zhifubaoName + '\n\n收款账号：' + that.zhifubao + '',
								success: (e) => {
									if (e.confirm) {
										this.$queue.showLoading("提现中...");
										this.$Request.getT("/cash/out/" + userId).then(res => {
											if (res.status === 0 && res.data) {
												that.$queue.showToast("提现申请成功，预计三个工作日到账");
												that.getMoney();
											}
											uni.hideLoading();
										});
									}
								}
							});
						} else {
							this.$queue.showToast("提现金额必须大于或等于10元才可提现");
						}
					} else {
						uni.navigateTo({
							url: "/pages/member/zhifubao"
						})
					}
				} else {
					uni.navigateTo({
						url: "/pages/public/login"
					})
				}
			},

		},

	}
</script>

<style lang='less'>
	@import "../static/css/index.css";

	.cash {
		text-align: center;
		background: white;
		height: 100%;
		position: absolute;
		width: 100%;

		.cash-top {
			padding: 32upx 32upx 50upx 32upx;
			/* border-bottom: 1px solid gainsboro; */
			background: #e10a07;
		}

		.leiji {
			font-size: 14px;
			color: #FFFFFF;
			margin-bottom: 10px;
		}
    .content {
	display: flex;
	flex-direction: column;
	justify-content:center;
	/* margin-top: 128upx; */
}

/* 头部 logo */
.header {
	text-align: center;

	width:161upx;
	height:161upx;
	box-shadow:0upx 0upx 60upx 0upx rgba(0,0,0,0.1);
	border-radius:50%;
	background: -moz-linear-gradient(left, #F15B6C, #e10a07 100%);
	background: -webkit-gradient(linear, left top, left right, color-stop(0, #F15B6C), color-stop(100%, #e10a07));
	background: -webkit-linear-gradient(left, #F15B6C 0, #e10a07 100%);
	background: -o-linear-gradient(left, #F15B6C 0, #e10a07 100%);
	background: -ms-linear-gradient(left, #F15B6C 0, #e10a07 100%);
	background: linear-gradient(to left, #F15B6C 0, #e10a07 100%);
	margin-top: 180upx;
	margin-bottom: 72upx;
	font-size: 60upx;
	color: white;
	font-weight: bold;
	padding-top: 32upx;
	margin-left: auto;
	margin-right: auto;
}
.header image{
	width:161upx;
	height:161upx;
	border-radius:50%;
}

/* 主体 */
.main {
	display: flex;
	flex-direction: column;
	padding-left: 70upx;
	padding-right: 70upx;
}
.tips {
	color: #999999;
	font-size: 28upx;
	margin-top: 64upx;
	margin-left: 48upx;
}

/* 其他登录方式 */
.other_login{
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	margin-top: 256upx;
	text-align: center;
}
.login_icon{
	border: none;
	font-size: 64upx;
	margin: 0 64upx 0 64upx;
	color: rgba(0,0,0,0.7)
}
.wechat_color{
	color: #83DC42;
}
.weibo_color{
	color: #F9221D;
}
.github_color{
	color: #24292E;
}

/* 底部 */
.footer{
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	font-size: 28upx;
	margin-top: 64upx;
	color: rgba(0,0,0,0.7);
	text-align: center;
	height: 40upx;
	line-height: 40upx;
}
.footer text{
	font-size: 24upx;
	margin-left: 15upx;
	margin-right: 15upx;
}
	}
</style>
