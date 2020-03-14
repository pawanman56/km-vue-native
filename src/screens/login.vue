
<template>
  <nb-container v-if="!loaded" :style="{backgroundColor: '#fff'}">
    <nb-header>
      <nb-body>
        <nb-title>Login</nb-title>
      </nb-body>
    </nb-header>

    <nb-content padder>
      <nb-form>
          <nb-item>
            <nb-input placeholder="Email"/>
          </nb-item>
          <nb-item last>
            <nb-input placeholder="Password"/>
          </nb-item>
        </nb-form>
        <view :style="{marginTop:10}">
          <nb-button block>
            <nb-text>Login</nb-text>
          </nb-button>
        </view>
    </nb-content>
  </nb-container>

  <nb-spinner v-else></nb-spinner>
</template>

<script>
export default {
  data: function() {
    return {
      emailValue: '',
      password: '',
      loaded: false
    };
  },

  created() {
  },

  methods: {
    login() {
    }
  }
};
</script>
