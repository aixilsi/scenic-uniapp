<template>
  <view class="page">
    <view class="card">
      <view class="h1">鐢靛瓙瀵兼父</view>
      <view class="desc">鐐瑰嚮杩涘叆 H5 瀵兼父锛堟渶鐪侀挶銆佹渶绋筹級</view>
    </view>

    <view class="list">
      <view class="item" @click="open('TAQINGGONG')">
        <view class="name">澶竻瀹?/view>
        <view class="sub">H5 瀵兼父</view>
      </view>
      <view class="item" @click="open('MINGDAOGONG')">
        <view class="name">鏄庨亾瀹?/view>
        <view class="sub">H5 瀵兼父</view>
      </view>
    </view>

    <view class="tip">WebView 涓氬姟鍩熷悕闇€閰嶇疆锛歮all.leyoobao.com</view>
  </view>
</template>

<script>
import { LINKS } from "@/common/links"
export default {
  methods: {
    open(key) {
      const url = LINKS.GUIDE[key]
      uni.navigateTo({ url: `/pages/webview/index?title=${encodeURIComponent("鐢靛瓙瀵兼父")}&url=${encodeURIComponent(url)}` })
    }
  }
}
</script>

<style>
.page{padding:28rpx;min-height:100vh;box-sizing:border-box;background:#f7f8fa;}
.card{background:#fff;border-radius:20rpx;padding:26rpx;}
.h1{font-size:40rpx;font-weight:800;color:#111;}
.desc{margin-top:10rpx;font-size:26rpx;color:#666;line-height:1.6;}
.list{margin-top:18rpx;}
.item{background:#fff;border-radius:18rpx;padding:22rpx;margin-bottom:14rpx;}
.name{font-size:32rpx;font-weight:800;color:#111;}
.sub{margin-top:8rpx;font-size:26rpx;color:#666;}
.tip{margin-top:16rpx;font-size:24rpx;color:#999;line-height:1.5;}
</style>
