
<template>
  <view class="container">
    <index />
  </view>
</template>

<script>
import Vue from 'vue-native-core';
import { VueNativeBase } from 'native-base';
import Index from './index';

Vue.use(VueNativeBase);

export default {
  components: { Index }
};
</script>

<style>
.container {
  flex: 1;
}
</style>