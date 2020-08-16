<template>
	<view>
		<!-- 轮播图 -->
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="200" style="height: 250rpx;">
			<swiper-item>
				<image src="/static/img/banner/1.jpg" style="width: 100%;"></image>
			</swiper-item>
			<swiper-item>
				<image src="/static/img/banner/2.jpg" style="width: 100%;"></image>
			</swiper-item>
		</swiper>
		<ZhuboCards :data="zhuboData" />
	</view>
</template>

<script lang="ts">
	import ZhuboCards, { ZhuboCard } from './zhubo_cards.vue'
	
	const data: ZhuboCard[] = [
		new ZhuboCard('/static/img/zhubo/1.jpg', 2, 2, '小花', '直播中'),
		new ZhuboCard('/static/img/zhubo/1.jpg', 2, 2, '小花', '直播中'),
		new ZhuboCard('/static/img/zhubo/1.jpg', 2, 2, '小花', '直播中'),
		new ZhuboCard('/static/img/zhubo/1.jpg', 2, 2, '小花', '直播中')
	]
	export default Vue.extend({
		components: { ZhuboCards },
		data() {
			return {
				zhuboData: data
			}
		},
		onLoad() {

		},
		methods: {

		}
	})
</script>

<style>

</style>
