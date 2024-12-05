<template>
  <div class="signup">
      <div class="signup-1">
          <h2 class="sign-up-title">Sign Up</h2>
          <div class="content">
              <div class="inputs">
                  <div class="input-group">
                      <input type="text" id="username" v-model="username" placeholder="Enter your username" />
                  </div>
                  <div class="input-group">
                      <input type="email" id="email" v-model="email" placeholder="Enter your email" />
                  </div>
                  <div class="input-group">
                      <input type="password" id="password" v-model="password" placeholder="Enter your password" />
                  </div>
                  <div class="input-group">
                      <input type="text" id="app-key" v-model="appKey" placeholder="Enter your App key" />
                  </div>
                  <div class="input-group">
                      <input type="text" id="secret-key" v-model="secretKey" placeholder="Enter your Secret key" />
                  </div>
              </div>
              <div class="text">
                  <input type="checkbox" id="terms" v-model="agreeToTerms" />
                  <label for="terms">
                      I have read and agree to the <a href="#">privacy policy and terms</a>.
                  </label>
              </div>
              <div class="text">
                <input type="checkbox" id="account-type" v-model="accountType" />
                  <label for="account-type">
                    Mock Account (Virtual Account)
                  </label>
              </div>
          </div>
      </div>
      <div class="bottom">
          <button class="button" :disabled="!formIsValid" @click="handleSignUp">Sign Up</button>
          <button class="button_close" @click="$emit('close')">Cancel</button>
      </div>
  </div>
</template>

<script lang="ts">
export default {
  data() {
      return {
          username: '',
          email: '',
          password: '',
          appKey: '',
          secretKey: '',
          agreeToTerms: false,
          accountType: '',
      };
  },
  computed: {
      formIsValid() {
          return this.username && this.email && this.password && this.appKey && this.secretKey && this.agreeToTerms && this.accountType;
      },
  },
  methods: {
      handleSignUp() {
          console.log('User data:', {
              username: this.username,
              email: this.email,
              password: this.password,
              appKey: this.appKey,
              secretKey: this.secretKey,
              accountType: this.accountType,
          });
          this.$emit('close'); // 모달 닫기 요청
      },
  },
};
</script>

<style scoped>
.signup {
  width: 600px;
  height: 560px;
  margin: auto;
  margin-top: 3vh;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  gap: 100px;
  padding: 48px;
  background: #FFFFFF;
  box-sizing: content-box;
  border: 1px solid #000000;
  
}
.signup .signup-1 {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  row-gap: 24px;
}
.signup .signup-1 .sign-up-title {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 36px;
  color: #4C4C57;
  font-family: "Open Sans";
  font-size: 28px;
  line-height: 36px;
  font-weight: 700;
  row-gap: 24px;
}
.signup .signup-1 .content {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 280px;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  row-gap: 32px;
}
.signup .signup-1 .content .inputs {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 230px;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  row-gap: 16px;
  .input-group {
    width: 100%;
    height: 52px;
    input{
      width: 100%;
      height: 100%;
      border-width: 0 0 1px;
      outline: none;
    }
  }
}
.signup .signup-1 .content .text {
  flex-shrink: 0;
  align-self: stretch;
  width: 601px;
  height: 16px;
  display: flex;
  flex-direction: row;
  justify-content: start;
  align-items: start;
  column-gap: 8px;
}
.signup .signup-1 .content .text #terms, #account-type {
  flex-shrink: 0;
  width: 16px;
  height: 16px;
  margin-top: 2px;
  border-radius: 4px;
  overflow: hidden;
  background: #FFFFFF;
  border: 1px solid #B8B8C1;
}
.signup .signup-1 .content .text .i-have-read-and-agree-to-the-privacy-policy-and-terms {
  flex-grow: 1;
  width: 577px;
  height: 16px;
  color: #3578FF;
  font-family: "Open Sans";
  font-size: 12px;
  line-height: 16px;
  font-weight: 400;
}
.signup .signup-1 .content .text .i-have-read-and-agree-to-the-privacy-policy-and-terms > div {
  width: 100%;
}
.signup .signup-1 .content .text .i-have-read-and-agree-to-the-privacy-policy-and-terms > div span:nth-child(2) {
  font-family: "Source Sans Pro";
}
.signup .bottom {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 92px;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  row-gap: 10px;
}
.signup .bottom .button {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 48px;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  background: #A0A4F2;
  color: #000000;
  border-width: 0;
  cursor: pointer;
}
.signup .bottom .button:disabled{
  cursor: not-allowed;
  background-color: #C1C3F4;
}
.button_close{
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 48px;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  background: #f2f2f2;
  border-width: 0;
  cursor: pointer;
}
</style>