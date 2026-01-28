<template>
  <view class="page">
    <view class="card">
      <view class="h1">鏅尯灏忕▼搴忥紙MVP锛?/view>
      <view class="desc">棰勭畻 3000 鐨勬渶灏忓疄鐜帮細瀵兼父 / 璐エ / 鍏憡 / 閫氱煡 / 鎹愭</view>
      <view class="btns">
        <button class="btn" @click="goGuide">鐢靛瓙瀵兼父</button>
        <button class="btn outline" @click="goTicket">绔嬪嵆璐エ</button>
      </view>
    </view>

    <view class="card" style="margin-top:20rpx;">
      <view class="h2">蹇嵎鍏ュ彛</view>
      <view class="grid">
        <view class="item" @click="goInfo">瀹樻柟淇℃伅</view>
        <view class="item" @click="goNotice">閫氱煡</view>
        <view class="item" @click="goDonate">鏉庢皬绁犲爞鎹愭</view>
        <view class="item" @click="goRank">鎹愭鎺掕姒?/view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  methods: {
    goGuide() { uni.switchTab({ url: "/pages/guide/index" }) },
    goTicket() { uni.switchTab({ url: "/pages/webview/index" }) },
    goInfo() { uni.navigateTo({ url: "/pages/info/list" }) },
    goNotice() { uni.navigateTo({ url: "/pages/notice/list" }) },
    goDonate() { uni.navigateTo({ url: "/pages/donate/index" }) },
    goRank() { uni.navigateTo({ url: "/pages/donate/rank" }) }
  }
}
</script>

<style>
.page{padding:28rpx;min-height:100vh;box-sizing:border-box;background:#f7f8fa;}
.card{background:#fff;border-radius:20rpx;padding:26rpx;}
.h1{font-size:40rpx;font-weight:800;color:#111;}
.desc{margin-top:10rpx;font-size:26rpx;color:#666;line-height:1.6;}
.btns{display:flex;gap:18rpx;margin-top:18rpx;}
.btn{flex:1;border-radius:16rpx;background:#111;color:#fff;font-size:30rpx;}
.btn.outline{background:#fff;color:#111;border:2rpx solid #111;}
.h2{font-size:30rpx;font-weight:700;color:#111;}
.grid{display:flex;flex-wrap:wrap;margin-top:16rpx;gap:12rpx;}
.item{width:calc(50% - 6rpx);padding:20rpx;border-radius:16rpx;background:#f3f4f6;color:#111;font-size:28rpx;}
</style>
