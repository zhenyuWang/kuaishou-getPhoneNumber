<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<button type="primary" open-type="getPhoneNumber" @getphonenumber="getphonenumber">
			<view>测试子元素</view>
			<view>getPhoneNumber</view>
		</button>
	</view>
</template>

<script setup>
	import {
		ref
	} from 'vue'
	
	const title = ref('Hello')
	const getphonenumber = (e) => {
		console.log('getPhoneNumber', e)
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
