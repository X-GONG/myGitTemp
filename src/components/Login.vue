<template>
  <div class="login_container">
    <div class="login_box">
      <div class="avatar_box">
        <img src="../assets/logo.png">
      </div>
      <el-form ref="form" :model="form" class="login_form">
        <el-form-item>
          <el-input v-model="form.name">
            <i slot="prefix" class="el-icon-s-custom"></i>
          </el-input>
        </el-form-item>
        <el-form-item>
          <el-input v-model="form.name">
            <i slot="prefix" class="el-icon-s-goods"></i>
          </el-input>
        </el-form-item>
        <el-form-item class="sumbit_btn">
          <el-button @click="sumbit">提交</el-button>
          <el-button @click="refrest">重置</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      form: {}
    }
  },
  methods: {
    sumbit() {
      window.sessionStorage.setItem('token','xgong123')
      this.$router.push({
        path: '/home'
      })
    },
    refrest() {}
  }
}
</script>
<style lang="less" scoped>
.login_container {
  height: 100%;
  background: #2b4b6b;
}
.login_box {
  width: 450px;
  height: 300px;
  background: #fff;
  border-radius: 3px;
  /* 水平垂直居中 */
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  .avatar_box {
    height: 130px;
    width: 130px;
    border-radius: 50%;
    padding: 10px;
    box-shadow: 0 0 10px #ddd;
    position: absolute;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #eee;
    img {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background-color: #eee;
    }
  }
  .login_form {
    position: absolute;
    bottom: 0;
    width: 100%;
    padding: 0 20px;
    box-sizing: border-box;
  }
  .sumbit_btn {
    // position: absolute;
    // bottom: 5px;
    // left: 50%;
    // transform: translate(-50%);
    text-align: center;
  }
}
</style>
