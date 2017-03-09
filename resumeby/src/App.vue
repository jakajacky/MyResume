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
          <img src="./assets/person.png" style="width:24px;">
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
        <div class="">
          <img src="./assets/person.png">
        </div>
        <div class="grid-content bg-purple">
          <p style="margin-top:10px;color:#FFA500">2014-10~2015-07</p>
          <el-tag type="warning">青岛联创优内科技有限公司</el-tag>
          <el-tag type="primary">.NET开发</el-tag>
          <el-tag type="success">iOS开发</el-tag>
        </div>

      </el-col>
    </el-row>

  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
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
