<script>
import Modal from './Modal.vue';
import SignUp from './SignUpModal.vue';
import Password from './ForgotPasswordModal.vue'

export default {
    components: {
        Modal,
        SignUp,
        Password,
    },
    data() {
        return {
            showSignUpModal: false, // 모달 표시 여부
            showFindPwModal: false,
        };
    },
    methods: {
        closeModal() {
            this.showSignUpModal = false; // 모달 닫기
            this.showFindPwModal = false;
        },
    },
};
</script>

<template>
    <div class="login">
        <div class="form">
            <img src="https://image-resource.creatie.ai/143979859576639/143979859576648/59c313bd0c486b3ab767d842246a9adf.png" class="image" />
            <div class="login-1">
                <div class="inputs">
                    <div class="input">
                        <input type="email" placeholder="Enter your email" />
                    </div>
                    <div class="input-1">
                        <input type="password" placeholder="Enter your password" />
                    </div>
                    <div class="text">
                        <span class="forgot-password" @click="showFindPwModal = true">Forgot password</span>
                    </div>
                </div>
                <div class="bottom">
                    <button class="button login-2">Login</button>
                    <div class="text-1">
                        <span class="dont-have-account">Don't have an account?</span>
                        <span class="sign-up" @click="showSignUpModal = true">Sign up</span>
                    </div>
                </div>
            </div>
        </div>
        <!-- 모달창 -->
        <Modal v-if="showSignUpModal" @close="closeModal">
            <SignUp @close="closeModal" />
        </Modal>
        <Modal v-if="showFindPwModal" @close="closeModal">
            <Password @close="closeModal" />
        </Modal>
    </div>
</template>

<style scoped>
.login {
    display: flex;
    justify-content: center;
    align-items: center; 
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    background: rgba(187, 189, 242, 0.4);
}
.login .form {
  position: relative;
  margin: auto;
  width: 68%;
  height: max-content;
  border-radius: 50px;
  overflow: hidden;
  background: #FFFFFF;
}
.login .form .image {
  position: relative;
  width: 200px;
  height: 150px;
  margin-left: 27vw;
  object-fit: cover;
}
.login .form .login-1 {
  position: relative;
  width: 95%;
  height: 65%;
  margin: auto;
  margin-bottom: 20px;
  border-radius: 30px;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: center;
  row-gap: 45px;
  column-gap: 45px;
  padding: 24px 24px 72px 24px;
  background: #F7F7F8;
}
.login .form .login-1 .inputs {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  row-gap: 16px;
  column-gap: 16px;
    input {
        width: 100%;
        border-width: 0;
        background-color: #FFFFFF;
        outline: none;
  }
}
.login .form .login-1 .inputs .input {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: auto;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: start;
  row-gap: 10px;
  column-gap: 10px;
  padding: 16px;
  background: #FFFFFF;
}
.login .form .login-1 .inputs .input .email {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: auto;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  color: #91929F;
  font-family: "Open Sans";
  font-size: 14px;
  line-height: 20px;
  font-weight: 400;
}
.login .form .login-1 .inputs .input-1 {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: auto;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: start;
  row-gap: 10px;
  column-gap: 10px;
  padding: 16px;
  background: #FFFFFF;
}
.login .form .login-1 .inputs .input-1 .password {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: auto;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  color: #91929F;
  font-family: "Open Sans";
  font-size: 14px;
  line-height: 20px;
  font-weight: 400;
}
.login .form .login-1 .inputs .text {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: end;
  row-gap: 10px;
  column-gap: 10px;
}
.login .form .login-1 .inputs .text .forgot-password {
  flex-shrink: 0;
  width: 110px;
  height: 20px;
  white-space: nowrap;
  color: #91929F;
  font-family: "Open Sans";
  font-size: 14px;
  line-height: 20px;
  font-weight: 400;
  cursor: pointer;
}
.login .form .login-1 .bottom {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 84px;
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  row-gap: 16px;
  column-gap: 16px;
}
.login .form .login-1 .bottom .button {
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
  border-width: 0;
  cursor: pointer;
}
.login .form .login-1 .bottom .button .login-2 {
  flex-shrink: 0;
  width: 42px;
  height: 20px;
  white-space: nowrap;
  color: #FFFFFF;
  font-family: "Open Sans";
  font-size: 16px;
  line-height: 20px;
  font-weight: 600;
}
.login .form .login-1 .bottom .text-1 {
  flex-shrink: 0;
  align-self: stretch;
  width: 100%;
  height: 20px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  column-gap: 4px;
  row-gap: 0px;
}
.login .form .login-1 .bottom .text-1 .dont-have-account {
  flex-shrink: 0;
  max-width: 200px;
  height: 20px;
  white-space: nowrap;
  color: #91929F;
  font-family: "Open Sans";
  font-size: 14px;
  line-height: 20px;
  font-weight: 400;
}
.login .form .login-1 .bottom .text-1 .sign-up {
  flex-shrink: 0;
  width: 50px;
  height: 20px;
  white-space: nowrap;
  color: #050259;
  font-family: "Open Sans";
  font-size: 14px;
  line-height: 20px;
  font-weight: 600;
  cursor: pointer;
}
</style>