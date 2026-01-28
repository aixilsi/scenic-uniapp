<template>
  <view class="page">
    <view class="item" v-for="x in list" :key="x.id" @click="open(x.id)">
      <view class="t">{{x.title}}</view>
      <view class="s">{{x.time}}</view>
    </view>
  </view>
</template>

<script>
import { mockNotices } from "@/common/mock/data"
export default {
  data() { return { list: mockNotices } },
  methods: { open(id) { uni.navigateTo({ url: "/pages/notice/detail?id=" + id }) } }
}
</script>

<style>
.page{padding:28rpx;min-height:100vh;background:#f7f8fa;box-sizing:border-box;}
.item{background:#fff;border-radius:18rpx;padding:22rpx;margin-bottom:14rpx;}
.t{font-size:30rpx;font-weight:800;color:#111;}
.s{margin-top:8rpx;font-size:26rpx;color:#666;}
</style>
