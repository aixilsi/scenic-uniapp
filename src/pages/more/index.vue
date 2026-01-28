<template>
  <view class="page">
    <view class="card">
      <view class="h1">鏇村</view>
      <view class="desc">瀹樻柟淇℃伅銆侀€氱煡銆佹崘娆剧瓑鍔熻兘鍏ュ彛</view>
    </view>

    <view class="list">
      <view class="row" @click="go('/pages/info/list')">
        <view class="t">瀹樻柟淇℃伅鍙戝竷</view>
        <view class="s">鍏憡 / 娲诲姩 / 鏀跨瓥</view>
      </view>
      <view class="row" @click="go('/pages/notice/list')">
        <view class="t">閫氱煡</view>
        <view class="s">璐エ鎴愬姛 / 娲诲姩鎻愰啋 / 绱ф€ラ€氱煡</view>
      </view>
      <view class="row" @click="go('/pages/donate/index')">
        <view class="t">鏉庢皬绁犲爞鎹愭</view>
        <view class="s">鏀寔鎵爜鐩磋揪</view>
      </view>
      <view class="row" @click="go('/pages/donate/rank')">
        <view class="t">鎹愭鎺掕姒?/view>
        <view class="s">鎹愬緱瓒婂瓒婇潬鍓?/view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  methods: { go(url) { uni.navigateTo({ url }) } }
}
</script>

<style>
.page{padding:28rpx;min-height:100vh;box-sizing:border-box;background:#f7f8fa;}
.card{background:#fff;border-radius:20rpx;padding:26rpx;}
.h1{font-size:40rpx;font-weight:800;color:#111;}
.desc{margin-top:10rpx;font-size:26rpx;color:#666;line-height:1.6;}
.list{margin-top:18rpx;}
.row{background:#fff;border-radius:18rpx;padding:22rpx;margin-bottom:14rpx;}
.t{font-size:30rpx;font-weight:800;color:#111;}
.s{margin-top:8rpx;font-size:26rpx;color:#666;}
</style>
