<template>
  <div class="document-bg">
    <div class="bg-plus">
      <el-container class="outer-container">
        <el-header height="60px" class="header">
          <div class="logo">
            <img src="../../assets/images/logo.png" height="60">
          </div>
          <p class="name">文档标题</p>
        </el-header>
        <el-container class="inner-container">
          <el-aside width="100px" class="leftPane">
            <p class="online-users">在线成员</p>
            <div>
              <el-avatar :size="50" class="icon"> user </el-avatar>
            </div>
            <div>
              <el-avatar :size="50" class="icon"> user </el-avatar>
            </div>
            <div>
              <el-avatar :size="50" class="icon"> user </el-avatar>
            </div>
          </el-aside>
          <el-main class="rightPane">
            <div class="editor">
              <QuillTest></QuillTest>
            </div>
          </el-main>
        </el-container>
      </el-container>
    </div>
  </div>
</template>

<script>
import QuillTest from "@/components/QuillTest";
export default {
  name: "DocumentEdit",
  components: {QuillTest}
}
</script>

<style scoped>
.document-bg {
  background-image: url("../../assets/images/sign-bg.jpg");
  background-repeat: repeat-y;
  min-height: 800px;
  overflow: hidden;
  background-position:center;
  background-size: 100% auto;
}
.bg-plus {
  background-color: rgba(255, 255, 255, 0.50);
  min-height: 800px;
  overflow: hidden;
  background-position:center;
  background-size: 100% auto;
}
.outer-container {
  height: 800px;
}
.inner-container {
  padding: 10px 0 20px 0;

}
.header {
  margin: 0 20px 0 20px;
  border-radius: 0 0 10px 10px;
  background-color: rgba(255, 255, 255, 0.30);
  overflow: hidden;
  box-shadow: 3px 3px 10px #bebebe;

}
.logo {
  position: absolute;
}
.name {
  position: center;
  font-size: 20px;
  margin-top: 15px;
}
.leftPane {
  margin: 0 0 0 20px;
  background-color: rgba(190, 190, 190, 0.25);
  border-radius: 10px;
  box-shadow: 3px 3px 10px #bebebe;
}
.icon {
  margin: 0 0 10px 0;
}
.rightPane {
  margin: 0 20px 0 20px;
  padding: 0;
}
.editor {
  height: 668px;
}
.online-users {

}
</style>