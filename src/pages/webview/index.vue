<template>
  <view class="page">
    <web-view :src="src"></web-view>
  </view>
</template>

<script>
import { LINKS } from "@/common/links"
export default {
  data() {
    return { src: LINKS.TICKET }
  },
  onLoad(query) {
    if (query && query.url) this.src = decodeURIComponent(query.url)
    if (query && query.title) uni.setNavigationBarTitle({ title: decodeURIComponent(query.title) })
    else uni.setNavigationBarTitle({ title: "璐エ" })
  }
}
</script>

<style>
.page{height:100vh;background:#fff;}
</style>
