
<template>
  <view class="container">
    <index />
  </view>
</template>

<script>
import Vue from 'vue-native-core';
import { VueNativeBase } from 'native-base';
import Meteor from 'react-native-meteor';
import Index from './index';

Vue.use(VueNativeBase);
Meteor.connect('ws://192.168.42.82:3000/websocket');

export default {
  components: { Index }
};
</script>

<style>
.container {
  flex: 1;
}
</style>