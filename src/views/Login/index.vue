<template>
  <div class="login">
      <img src="../../assets/aside.png" alt="">
      <el-card class="card">
          <el-form :model='obj' :rules='rules' ref='text'>
              <div class="logo"></div>
              <el-form-item prop='number'>
              <el-input placeholder='请输入账号'
              prefix-icon="el-icon-user-solid" 
              v-model='obj.number'></el-input>
              </el-form-item>

               <el-form-item prop='password'>
               <el-input placeholder='请输入密码' prefix-icon="el-icon-lock" 
               v-model='obj.password' type='password'></el-input>

              </el-form-item>
          </el-form>
          <el-button class="btn">登录</el-button>
      </el-card>
      <h3 class="footer">智猪网络</h3>
  </div>
</template>

<script>
export default {
    data(){
        return{
            obj:{
                number:'admin',
                password:''
            },
            rules:{
                number:[{required:true,message:'填写手机号'}],
                password:[{required:true,message:'填写密码'}],
            }
        }
    }
}
</script>

<style scoped lang='less'>
.login{
    width: 100vw;
    height: 100vh;
    background-color: #231e6a;
    img{
        position: fixed;
        top: 200px;
        left: 155px;
        height: 400px;
    }
    .card{
        width: 382px;
        height: 455px;
        position: fixed;
        top: 157px;
        right: 158px;
        border-radius: 20px;
        padding: 70px 36px 57px 36px;
        box-sizing: border-box;
        .logo{
            height: 56px;
            background: url('../../assets/logo.png') no-repeat;
            margin-bottom: 64px;
            margin-left: 24px;
        }
        .btn{
            width: 100%;
            background-color: #975ae1;
            color: azure;
            margin-top: 20px;
        }
    }
    .footer{
        position: fixed;
        bottom: 20px;
        left: 495px;
        color:white
    }
}

</style>