<template>
	<view class="theme-item">
		<navigator url="" class="box" v-if="!isMore"	>
			<image class="pic" src="../../common/images/col.jpeg" mode="aspectFill"></image>
			<view class="mask">
				星穹铁道
			</view>
			<view class="tab">
				3天前更新
			</view>
		</navigator>
		
		<navigator url="" class="box more" v-else>
			<image class="pic" src="../../common/images/mask.jpeg" mode="aspectFill"></image>
			<view class="mask">
				<uni-icons type="more-filled" size="34" color="#fff"></uni-icons>
				<view class="text">更多</view>
			</view>
		</navigator>
	</view>
</template>

<script setup>
	defineProps({
		isMore: {
			type: Boolean,
			default: false
		}
	})
</script>

<style lang="scss" scoped>
	.theme-item {
		.box {
			height: 340rpx;
			border-radius: 15rpx;
			overflow: hidden;
			position: relative;
			.pic {
				width: 100%;
				height: 100%;
			}
			.mask {
				position: absolute;
				left: 0;
				bottom: 0;
				width: 100%;
				height: 70rpx;
				font-size: 30rpx;
				font-weight: 600;
				color: #fff;
				background: rgba(0, 0 ,0 ,0.2);
				display: flex;
				justify-content: center;
				align-items: center;
				backdrop-filter: blur(20rpx);
			}
			.tab {
				position: absolute;
				left: 0;
				top: 0;
				background: rgba(250, 129, 90, 0.7);
				backdrop-filter: blur(20rpx);
				color: #fff;
				font-size: 22rpx;
				padding: 6rpx 14rpx;
				border-radius: 0 0 15rpx 0;
				transform: scale(0.8);
				transform-origin: left top;
			}
		}
		.box.more {
			.mask {
				width: 100%;
				height: 100%;
				flex-direction: column;
			}
			.text {
				font-size: 28rpx;
			}
		}
	}

</style>