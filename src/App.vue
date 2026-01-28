<template>
  <view class='app'>
    <slot />
  </view>
</template>

<script>
export default {
  onLaunch() {
    console.log('App Launch')
  }
}
</script>

<style>
.app {
  min-height: 100vh;
  background: #f7f8fa;
}
</style>
