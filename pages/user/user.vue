<template>
	<view class="userLayout">
		<view class="userInfo">
			<view class="avatar">
				<img src="../../static/avatar.jpeg"  mode="aspectFill"/>
			</view>
			<view class="ip">
				100.100.100.100
			</view>
			<view class="address">
				来自于：武汉
			</view>
		</view>
		<view class="section">
			<view class="list">
				<view class="row" v-for="item in 3">
					<view class="left">
						<uni-icons type="download-filled" size="20" color="#28b389"></uni-icons>
						<view class="text">
							我的下载
						</view>
					</view>
					<view class="right">
						<view class="text">
							33
						</view>
						<uni-icons type="right" size="15" color="#aaa"></uni-icons>
					</view>
				</view>
			</view>
		</view>
		<view class="section">
			<view class="list">
				<view class="row" v-for="item in 2">
					<view class="left">
						<uni-icons type="download-filled" size="20" color="#28b389"></uni-icons>
						<view class="text">
							我的下载
						</view>
					</view>
					<view class="right">
						<view class="text">
							33
						</view>
						<uni-icons type="right" size="15" color="#aaa"></uni-icons>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
	.userLayout {
		.userInfo {
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			padding: 50rpx 0;
			.avatar {
				width: 160rpx;
				height: 160rpx;
				border-radius: 50%;
				overflow: hidden;
				image{
					width: 100%;
					height: 100%;
				}
			}
			.ip {
				font-size: 40rpx;
				color: #333;
				padding: 20rpx 0 5rpx;
			}
			.address {
				font-size: 28rpx;
				color: #aaa;
			}
		}
		.section {
			width: 690rpx;
			margin: 50rpx auto;
			border: 1px solid #eee;
			border-radius: 10rpx;
			box-shadow: 0 0 30rpx rgba(0, 0, 0, 0.05);
			.list {
				.row {
					display: flex;
					justify-content: space-between;
					align-items: center;
					padding: 0 30rpx;
					height: 100rpx;
					border-bottom: 1px solid #eee;
					&:last-child{
						border-bottom: 0;
					}
					.left {
						display: flex;
						align-items: center;
						.text {
							padding-left: 20rpx;
							color: #666;
						}
					}
					.right {
						display: flex;
						align-items: center;
						.text {
							font-size: 28rpx;
							color: #aaa;
						}
					}
				}
			}
		}
	}
</style>
