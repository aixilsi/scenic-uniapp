<template>
  <view class="page">
    <view class="card">
      <view class="h1">鏉庢皬绁犲爞鎹愭</view>
      <view class="desc">鏈€灏忓疄鐜帮細鍏堝仛椤甸潰 + 鎺掕姒滃崰浣嶏紝鍚庣画鎺ュ井淇℃敮浠樹笌钀藉簱</view>

      <view class="field">
        <view class="label">鎹愭閲戦锛堝厓锛?/view>
        <input class="inp" type="number" v-model="amount" placeholder="渚嬪锛?0" />
      </view>

      <button class="btn" @click="donate">绔嬪嵆鎹愭锛堝崰浣嶏級</button>
      <button class="btn outline" @click="goRank">鏌ョ湅鎺掕姒?/button>
    </view>

    <view class="tip">闂幆鐗堝缓璁細寰俊浜戝紑鍙?+ 鏀粯鍥炶皟鍐欏叆鎹愭璁板綍 + 鎺掕姒滆仛鍚堟煡璇€?/view>
  </view>
</template>

<script>
export default {
  data() { return { amount: "" } },
  methods: {
    donate() {
      const n = Number(this.amount || 0)
      if (!n || n <= 0) return uni.showToast({ title: "璇疯緭鍏ラ噾棰?, icon: "none" })
      uni.showModal({ title: "鍗犱綅鎻愮ず", content: "灏嗘潵杩欓噷浼氭媺璧峰井淇℃敮浠樸€傚綋鍓嶉噾棰濓細" + n + " 鍏?, showCancel: false })
    },
    goRank() { uni.navigateTo({ url: "/pages/donate/rank" }) }
  }
}
</script>

<style>
.page{padding:28rpx;min-height:100vh;background:#f7f8fa;box-sizing:border-box;}
.card{background:#fff;border-radius:20rpx;padding:26rpx;}
.h1{font-size:34rpx;font-weight:900;color:#111;}
.desc{margin-top:10rpx;font-size:26rpx;color:#666;line-height:1.6;}
.field{margin-top:18rpx;}
.label{font-size:26rpx;color:#333;}
.inp{margin-top:10rpx;background:#f3f4f6;border-radius:16rpx;padding:20rpx;font-size:28rpx;}
.btn{margin-top:16rpx;border-radius:16rpx;background:#111;color:#fff;font-size:30rpx;}
.btn.outline{background:#fff;color:#111;border:2rpx solid #111;}
.tip{margin-top:16rpx;font-size:24rpx;color:#999;line-height:1.5;}
</style>
