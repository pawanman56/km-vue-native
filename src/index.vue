
<template>
  <root>
    <login-screen />
  </root>
</template>

<script>
import { Root } from 'native-base';
import LoginScreen from './screens/login';

export default {
  components: { Root, LoginScreen }
};
</script>