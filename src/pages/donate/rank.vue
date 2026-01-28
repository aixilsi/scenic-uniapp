<template>
  <view class="page">
    <view class="item" v-for="(x,i) in list" :key="i">
      <view class="left">
        <view class="rank">NO.{{i+1}}</view>
        <view class="name">{{x.name}}</view>
      </view>
      <view class="amount">楼 {{x.amount}}</view>
    </view>
  </view>
</template>

<script>
import { mockDonateRank } from "@/common/mock/data"
export default { data() { return { list: mockDonateRank } } }
</script>

<style>
.page{padding:28rpx;min-height:100vh;background:#f7f8fa;box-sizing:border-box;}
.item{background:#fff;border-radius:18rpx;padding:22rpx;margin-bottom:14rpx;display:flex;align-items:center;justify-content:space-between;}
.left{display:flex;align-items:center;gap:14rpx;}
.rank{font-size:24rpx;color:#999;}
.name{font-size:30rpx;font-weight:900;color:#111;}
.amount{font-size:30rpx;font-weight:900;color:#111;}
</style>
