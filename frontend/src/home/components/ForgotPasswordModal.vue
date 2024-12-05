<template>
    <div class="signup">
        <div class="email">
            <div class="forgot-password">
                Forgot password?
            </div>
            <div class="content">
                <div class="inputs">
                    <div class="receive-by-email">
                        Receive by email
                    </div>
                    <div class="input-group">
                      <input type="text" id="username" v-model="E_username" placeholder="Username" />
                    </div>
                    <div class="input-group">
                      <input type="email" id="email" v-model="E_email" placeholder="Email" />
                  </div>
                </div>
            </div>
        </div>
        <div class="bottom">
            <div class="button">
                <button class="button" >Submit</button>
            </div>
        </div>
        <div class="or">
            Or
        </div>
        <div class="content-1">
            <div class="inputs-1">
                <div class="reset-password">
                    Reset password
                </div>
                <div class="input-group">
                      <input type="text" id="username" v-model="R_username" placeholder="Username" />
                </div>
                <div class="input-group">
                      <input type="text" id="username" v-model="R_secret_key" placeholder="Secret key" />
                </div>
            </div>
        </div>
        <div class="bottom">
            <button class="button" >Submit</button>
            <!-- <button class="button_close" @click="$emit('close')">Cancel</button> -->
        </div>
        <hr />
    </div>
</template>

<script lang="ts">
export default {
    data() {
      return {
        E_username: '',
        E_email: '',
        R_username: '',
        R_secret_key: '',
      };
  },
};
</script>

<style scoped>
.signup {
    /* position: absolute; */
    width: 600px;
    height: 560px;
    margin: auto;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: start;
    row-gap: 24px;
    padding: 48px;
    background: #FFFFFF;
    box-sizing: content-box;
    border: 1px solid #000000;
    .email {
        flex-shrink: 0;
        align-self: stretch;
        width: 100%;
        height: 200px;
        display: flex;
        flex-direction: column;
        justify-content: start;
        align-items: start;
        .forgot-password {
            flex-shrink: 0;
            align-self: stretch;
            width: 100%;
            height: 36px;
            color: #4C4C57;
            font-family: "Open Sans";
            font-size: 28px;
            line-height: 36px;
            font-weight: 700;
        }
        .content {
            flex-shrink: 0;
            align-self: stretch;
            width: 100%;
            height: 156px;
            display: flex;
            flex-direction: column;
            justify-content: start;
            align-items: start;
            row-gap: 32px;
            column-gap: 32px;
            .inputs {
                flex-shrink: 0;
                align-self: stretch;
                width: 100%;
                height: 156px;
                display: flex;
                flex-direction: column;
                justify-content: start;
                align-items: start;
                row-gap: 8px;
                column-gap: 8px;
                .receive-by-email {
                    flex-shrink: 0;
                    align-self: stretch;
                    width: 100%;
                    height: 36px;
                    color: #4C4C57;
                    font-family: "Open Sans";
                    font-size: 18px;
                    line-height: 36px;
                    font-weight: 600;
                }
            }
        }
    }
    .or {
        flex-shrink: 0;
        width: 100%;
        height: 20px;
        color: #3D3D3D;
        font-family: "Inter";
        font-size: 16px;
        line-height: 19px;
        font-weight: 400;
        text-align: center;
    }
    .content-1 {
        flex-grow: 1;
        width: 100%;
        height: 140px;
        display: flex;
        flex-direction: column;
        justify-content: start;
        align-items: start;
        row-gap: 24px;
        column-gap: 24px;
        .inputs-1 {
            flex-shrink: 0;
            align-self: stretch;
            width: 100%;
            height: 130px;
            display: flex;
            flex-direction: column;
            justify-content: start;
            align-items: start;
            row-gap: 8px;
            column-gap: 8px;
            .reset-password {
                flex-shrink: 0;
                align-self: stretch;
                width: 100%;
                height: 36px;
                color: #4C4C57;
                font-family: "Open Sans";
                font-size: 18px;
                line-height: 36px;
                font-weight: 600;
            }
        }
    }
}
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
.bottom {
        flex-shrink: 0;
        align-self: stretch;
        width: 100%;
        height: 48px;
        display: flex;
        flex-direction: column;
        justify-content: start;
        align-items: start;
        row-gap: 24px;
        column-gap: 24px;
}
.bottom .button {
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
    color: #FFFFFF;
    border-width: 0;
    cursor: pointer;
    font-family: "Open Sans";
    font-size: 16px;
    line-height: 20px;
    font-weight: 600;
}
/* .button_close{
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
} */
</style>