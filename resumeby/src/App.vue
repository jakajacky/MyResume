<template>
  <div id="app">
    <div class="bg" style="margin-top:-50px;height:250px;">
        <el-row type="flex" class="row-bg" justify="center" style="position:relative;top:160px;">
          <el-col :span="9"><div class="grid-content bg-purple"></div></el-col>
          <el-col :span="6">
            <div class="" style="text-align:center">
              <img style="width:150px;height:150px;border-radius:75px;justify:center;" src="./assets/icon.png">
            </div>

          </el-col>
          <el-col :span="9"><div class="grid-content bg-purple"></div></el-col>
        </el-row>
    </div>

    <el-row type="flex" class="row-bg" justify="center" style="position:relative;top:60px;">
      <el-col :span="11">
        <div class="" style="text-align:right;">
          <el-row type="flex" justify="end" style="margin-top:9px;">
            <el-col :span="2">
              <img src="./assets/person.png" style="width:24px;">
            </el-col>
            <el-col :span="4">
              <span>张小强</span>
            <el-col>
          </el-row>
        </div>
        <div class="" style="text-align:right;">
          <el-row type="flex" justify="end" style="margin-top:9px;">
            <el-col :span="2">
              <img src="./assets/location.png" style="width:24px;">
            </el-col>
            <el-col :span="4">
              <span>北京昌平</span>
            <el-col>
          </el-row>
        </div>
        <div class="grid-content bg-purple" style="text-align:right">
          <!-- <el-tag style="margin-top:5px;" type="gray">2014-10~2015-07</el-tag>
          <el-tag type="warning">青岛联创优内科技有限公司</el-tag>
          <el-tag type="primary">.NET开发</el-tag>
          <el-tag type="success">iOS开发</el-tag> -->
        </div>
      </el-col>
      <el-col :span="2">
        <div class="" style="text-align:center">
          <canvas id="myCanvas" width="15" height="510" style="border:1px solid #c3c3c3;">Your browser does not support the canvas element.
          </canvas>
        </div>
      </el-col>
      <el-col :span="11">
        <div class="" style="text-align:left;">
          <el-row type="flex" justify="start" style="margin-top:9px;">
            <el-col :span="2">
              <img src="./assets/phone.png" style="width:24px;">
            </el-col>
            <el-col :span="4">
              <span>18515982821</span>
            <el-col>
          </el-row>
        </div>
        <div class="" style="text-align:left;">
          <el-row type="flex" justify="start" style="margin-top:9px;">
            <el-col :span="2">
              <img src="./assets/mail.png" style="width:24px;">
            </el-col>
            <el-col :span="4">
              <span>zhangxiaoqiangjoe@gmail.com</span>
            <el-col>
          </el-row>
        </div>

        <div class="grid-content bg-purple">
          <p style="margin-top:62px;color:#FFA500">2015-10—现在</p>
          <el-tag type="warning">北京班德尔科技有限公司</el-tag>
          <el-tag type="success">iOS开发</el-tag>
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span style="line-height: 36px;"><font color=#FFA500>|</font> 构建帮助医药企业精准定位目标医生的移动化SFA管理工具</span>
              <el-button style="float: right;" type="text" icon="more" @click="showDetail"></el-button>
            </div>
            <transition name="fade">
              <div class="" v-show="show">
                <p><font color=#FFA500>|</font> 构建帮助医药企业精准定位目标医生的移动化SFA管理工具</p>
                <p><font color=#FFA500>|</font> 杨森LOC销售统计图表模块 Vue+ECharts重构</p>
                <p><font color=#FFA500>|</font> 发起并负责Jenkins+蒲公英自动化构建公司iOS项目</p>
                <p><font color=#FFA500>|</font> 使用蒲公英API，设计完成公司内部应用下载平台IDB Store</p>
                <p><font color=#FFA500>|</font> 葛兰素史克（以下简称GSK）HTTP/1.1后，完成与后台的HTTPS双向认证</p>
                <p><font color=#FFA500>|</font> 针对GSK新增安全测试，将GSK的项目作代码混淆处理，增加反编译难度</p>
                <p><font color=#FFA500>|</font> 重写公司所有项目使用的视频课程播放器，使用AVPlayer，支持画中画</p>
                <p><font color=#FFA500>|</font> 百度地图后台持续定位失败后的解决方案</p>
                <p><font color=#FFA500>|</font> 为Synapse平台设计完成公司内部直播推流测试工具</p>
                <p><font color=#FFA500>|</font> Novo Nordisk（以下简称NN）所有大区APP升级64位</p>
                <p><font color=#FFA500>|</font> NN 美洲区APP国际化功能更新</p>
                <p><font color=#FFA500>|</font> SQLite数据库迁移</p>
                <p><font color=#FFA500>|</font> 使用SQLCipher对所有项目本地数据库加密</p>
                <p><font color=#FFA500>|</font> GSK、NN、杨森的产品升级和维护</p>
                <p><font color=#FFA500>|</font> 肿么办 V1.0开发</p>
              </div>
          </transition>

          </el-card>

        </div>
        <!-- <div class="grid-content bg-purple">
          <p style="margin-top:10px;color:#FFA500">2014-10~2015-07</p>
          <el-tag type="warning">青岛联创优内科技有限公司</el-tag>
          <el-tag type="primary">.NET开发</el-tag>
          <el-tag type="success">iOS开发</el-tag>
        </div> -->

      </el-col>
    </el-row>

  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      show:false,
    }
  },
  methods: {
    showDetail:function(event) {
      console.log(event);
      this.show = !this.show
      this.$forceUpdate()
    }
  },
  mounted:function () {
    var array=["myCanvas","myCanvas1"]
    // for (var i = 0; i < array.length; i++) {
      var ca = array[0];
      var c=document.getElementById(ca);
      var cxt=c.getContext("2d");
      cxt.strokeStyle="#20B2AA";

      cxt.moveTo(7.5,0);
      cxt.lineTo(7.5,15);
      cxt.stroke();

      cxt.beginPath();
      cxt.arc(7,19,5,0,Math.PI*2,true);
      cxt.closePath();
      cxt.stroke();

      cxt.moveTo(7.5,23);
      cxt.lineTo(7.5,146);
      cxt.stroke();

      cxt.beginPath();
      cxt.arc(7,150,5,0,Math.PI*2,true);
      cxt.closePath();
      cxt.stroke();

      cxt.moveTo(7.5,154);
      cxt.lineTo(7.5,496);
      cxt.stroke();

  // var cxt=c.getContext("2d");
      // cxt.fillStyle="#FF0000";
      cxt.beginPath();
      cxt.arc(7.5,500,5,0,Math.PI*2,true);
      cxt.closePath();
      cxt.stroke();
    // cxt.fill()；
    // }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}

.bg {
  background-image: url("./assets/bg1.png");
  background-position: center;

}

.icon_person {

}

.box-card {
  width: 100%;
  margin-top: 10px;
}

/*过度动画*/
.fade-enter-active, .fade-leave-active {
  transition: opacity .25s ease-out
}

.fade-enter, .fade-leave-active {
  opacity: 0
}

/*.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-active {
  padding-left: 10px;
  opacity: 0;
}*/

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
