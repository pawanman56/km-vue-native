
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
            <nb-input placeholder="Email" v-model="emailValue" auto-capitalize="none"/>
          </nb-item>
          <nb-item last>
            <nb-input placeholder="Password" secure-text-entry v-model="password" auto-capitalize="none"/>
          </nb-item>
        </nb-form>
        <view :style="{marginTop:10}">
          <nb-button block :on-press='login'>
            <nb-text>Login</nb-text>
          </nb-button>
        </view>
    </nb-content>
  </nb-container>

  <nb-spinner v-else></nb-spinner>
</template>

<script>
import Meteor, { createContainer } from 'react-native-meteor';

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
      if (this.emailValue && this.password) {
        Meteor.loginWithPassword(this.emailValue.toLowerCase(), this.password, error => {
          if (error) {
            alert('Incorrect Email or Password.');
          }
        });
      } else {
        alert('Please enter existing email and password.');
      }
    }
  }
};
</script>
