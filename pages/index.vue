<template>
	<view class="container">
		<!--轮播-->
		<!-- <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true">
			<swiper-item>
				<view class="swiper-item">
					<image src="https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=2350817201,1137116540&fm=26&gp=0.jpg" class="banner-img"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=3545834692,4156954932&fm=26&gp=0.jpg" class="banner-img"></image>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item">
					<image src="https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=774373677,2313985244&fm=26&gp=0.jpg" class="banner-img"></image>
				</view>
			</swiper-item>
		</swiper> -->
		<!--列表-->
		<view class="list">

			<view v-for="i in item" :key="index">
				{{i.title}}
				{{i.text}}
				<!-- <view class="item" @tap="$toPage('/pages/article/detail')">
					<view class="title text-ellipsis">这里显示的是标题这里显示的是标题这里显示的是标题这里显示的是标题</view>
					<view class="content flex-row">
						<view class="info">
							<view class="summary">node是单线程的，是无法共享状态的是无法共享状态的是无法共享状态的是无法共享状态的是无法共享状态的是无法共享状态的。</view>
							<view class="flex-row">
								<text class="date">2021-05-06</text>
								<text class="views">200 阅读</text>
							</view>
						</view>
						<view class="cover">
							<image class="img" src="https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=1851283359,3457678391&fm=26&gp=0.jpg"></image>
						</view>
					</view>
				</view> -->
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			it = [{
				'title': '1',
				'text': '1'
			}, {
				'title': '2',
				'text': '2'
			}, {
				'title': '3',
				'text': '3'
			}, {
				'title': '4',
				'text': '4'
			}];
			return {
				item : it
			}
		},
		onLoad() {

		},
		methods: {

		},

	}
</script>

<style lang="scss" scoped>
	.swiper-item,
	.banner-img {
		width: 100%;
		height: 100%;
	}

	.item {
		padding: 30rpx;
		margin-bottom: 30rpx;
		background-color: #FFF;

		.title {
			font-weight: bold;
			padding-bottom: 30rpx;
			border-bottom: 2rpx solid #F5F5F5;
		}

		.content {
			padding-top: 30rpx;
			align-items: flex-start;

			.info {
				width: calc(100% - 160rpx);

				.summary {
					color: #777;
					height: 80rpx;
					font-size: 24rpx;
					line-height: 1.6;
					margin-bottom: 10rpx;
					@include text-ellipsis(2);
				}

				.date {
					font-size: 24rpx;
					color: $main-color;
					opacity: 0.6;
				}

				.views {
					color: #999;
					font-size: 24rpx;
				}
			}

			.cover {
				width: 140rpx;
				height: 120rpx;

				.img {
					width: 100%;
					height: 100%;
					border-radius: 4rpx;
				}
			}
		}
	}
</style>
