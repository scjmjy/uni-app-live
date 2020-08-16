<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
			const domModule = weex.requireModule('dom')
			domModule.addRule('fontFace', {
				'fontFamily': 'iconfont',
				'src': "url('/static/font/iconfont.ttf')"
			})
			
			uni.onTabBarMidButtonTap(function(){
				console.log('Tabbar mid button click')
			})
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import url("/static/css/common.css");
	@import url("/static/css/utils.css");
	/* #ifndef APP-PLUS-NVUE */
	@import url("/static/css/iconfont.css");
	/* #endif */
</style>
