<template>
  <view class="top-bar">
    <view class="title">
      <view class="left">
        <slot name="left" />
      </view>
      <view class="middle">
        <slot name="middle" />
      </view>
      <view class="right">
        <slot name="right" />
      </view>
    </view>
  </view>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  name: 'TopBar',
  setup(_, { root }) {
    return {}
  },
})
</script>

<style lang="scss">
.top-bar {
  padding-top: var(--status-bar-height);
  background: linear-gradient(45deg, #00dafe 10%, #00a8ff);
  color: white;

  .title {
    position: relative;
    display: flex;
    align-items: center;
    height: rpx(96);
    padding: 0 rpx(28);
    font-size: rpx(32);
    justify-content: space-between;
  }
}
</style>
