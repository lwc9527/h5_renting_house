<template>
  <div class="main">
    <div class="header vh-between">
      <span class="icon el-icon-arrow-left">理赔查询</span>
      <span class="icon"></span>
    </div>
    <div class="item-log">
        <el-form :model="loginParams" :rules="rules" ref="loginParams">
            <el-form-item prop="username" >
                <span class="laber">手机号码：</span>
                <el-input
                  v-model="loginParams.username"
                  maxlength="11"
                  placeholder="请输入手机号码"
                  clearable>
                  <i slot="prefix" class="user_icon"></i>
                </el-input>
            </el-form-item>
            <el-form-item prop="nick">
                <span class="laber">房东名称：</span>
                <el-input
                  v-model="loginParams.nick"
                  placeholder="请输入房东名称"
                  clearable>
                  <i slot="prefix" class="user_icon"></i>
                </el-input>
            </el-form-item>
            <div class="login-content mt-40">
              <bg-button
                className="blueWhite"
                width="100%"
                height="46px"
                :loading="BtnLoading"
                title="立即注册"
              ></bg-button>
            </div>
        </el-form>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      loginParams: {
        username: "",
        nick: "",
        password: "",
        password_confirm: "",
        code: "",
      },
    };
  },
  created () {
   
  },
  methods: {
   
  }
}
</script>
<style lang="scss" scoped>
.main {
    .item-log {
        width: 80%;
        margin: 20px auto 0;
        box-sizing: border-box;
        .laber{
            font-size: 14px;
        }
        .el-input__inner {
            color: #00C2FF;
            border: none;
            font-size:14px !important;
        }
        .el-button--success{
            width: 150px;
            height:34px;
            line-height:34px;
            font-size:13px;
            text-align: center;
            margin:0 2px;
            padding:0;
        }
        i {
            position: absolute;
            width: 24px;
            height: 24px;
            left: 1px;
            top: 50%;
            transform: translateY(-50%);
        }
        i.user_icon {
            background: url("~@a/images/icon-user-disable1@2x.png") no-repeat center;
            background-size: cover;
        }
        i.password_icon {
            background: url("~@a/images/icon-password-disable1@2x.png") no-repeat center;
            background-size: cover;
        }
        i.password_code {
            background: url("~@a/images/icon-code-disable1@2x.png") no-repeat center;
            background-size: cover;
        }
        &:hover {
            i.user_icon {
                background: url("~@a/images/icon-user-disable@2x.png") no-repeat center;
                background-size: cover;
            }
            i.password_icon {
                background: url("~@a/images/icon-password-disable@2x.png") no-repeat center;
                background-size: cover;
            }
            i.password_code {
                background: url("~@a/images/icon-code-disable@2x.png") no-repeat center;
                background-size: cover;
            }
        }
    }
}
</style>
