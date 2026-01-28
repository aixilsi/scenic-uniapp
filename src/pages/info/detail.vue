<template>
  <view class="page">
    <view class="card">
      <view class="h1">{{item.title}}</view>
      <view class="time">{{item.time}}</view>
      <view class="content">{{item.content}}</view>
    </view>
  </view>
</template>

<script>
import { mockAnnouncements } from "@/common/mock/data"
export default {
  data() { return { item: {} } },
  onLoad(q) {
    const id = q && q.id
    this.item = mockAnnouncements.find(x => x.id === id) || { title: "鏈壘鍒?, time: "", content: "" }
  }
}
</script>

<style>
.page{padding:28rpx;min-height:100vh;background:#f7f8fa;box-sizing:border-box;}
.card{background:#fff;border-radius:20rpx;padding:26rpx;}
.h1{font-size:34rpx;font-weight:900;color:#111;}
.time{margin-top:10rpx;font-size:24rpx;color:#999;}
.content{margin-top:18rpx;font-size:28rpx;color:#333;line-height:1.75;white-space:pre-wrap;}
</style>
