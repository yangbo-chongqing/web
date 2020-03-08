<template>
	<div>
	<div>
		<span>混编入门示例{{msg}}</span>
	</div>
	<a href="http://www.baidu.com">去百度</a>
	<image src="../../static/logo.png" style="width:100rpx;height:200rpx;"></image>
	<view :class="{ active: isActive }">111</view>
	<view class="static" v-bind:class="{ active: isActive, 'text-danger': hasError }">222</view>
	
	 <view v-for="(item,index) in rows" :key="item.id">
	            {{index +':'+ item.name}}
	 </view>
	<div id="example">
	  <p>原数据: "{{ message }}"</p>
	  <p>返转后数据: "{{ reversedMessage }}"</p>
	</div>
	<h1 v-if="awesome">Vue is awesome!</h1>
	<h1 v-else>Oh no 😢</h1>
	</div>
</template>

<script>
	export default {
		data(){
			return {
				msg:"我的心",
				isActive:true,
				hasError:true,
				rows:[{name:"东哥"},{name:"亮亮"}],
				message:"东哥",
				awesome:true
			}
		},
		computed: {
		    // 计算属性的 getter
		    reversedMessage: function () {
		      // `this` 指向 vm 实例
		      return this.message.split('').reverse().join('')
		    }
		  }
	}
</script>

<style>
	.active{
		color:red;
		
	}
	.text-danger{
		background-color: #0066CC;
	}
</style>
