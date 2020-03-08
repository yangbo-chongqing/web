<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
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
	/*每个页面公共css 注意每个文件后有分号*/
	@import "./common/uni.css";
	@import "./common/common.css";
	@import "./common/icon.css";
	@import "./common/animate.css";
	@import "./common/free.css"
</style>
