<template>
  <div class="hello">
    <el-container>
      <el-header class="myheader">
        <div class="myheaderSpan">
          <img src="../assets/00.png" class="myimg">
        </div>
        <div class="headerWenzi">供应商系统</div>
        <span class="myheaderRiget">
         
          <img src="../assets/1.png" class="myimg2">
        </span>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <el-row class="tac">
            <el-col>
              <el-menu
                default-active="2"
                class="el-menu-vertical-demo"
                @open="handleOpen"
                @close="handleClose"
              >
                <el-submenu index="1">
                  <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>系统首页</span>
                  </template>
                  <el-menu-item index="2">供应商</el-menu-item>
                </el-submenu>
              </el-menu>
            </el-col>
          </el-row>
        </el-aside>
        <el-container>
          <el-main>
            <template>
    <el-table
      :data="tableData"
      style="width: 100%">
      <el-table-column
        prop="date"
        label="日期"
        width="180">
      </el-table-column>
      <el-table-column
        prop="name"
        label="供应商"
        width="180">
      </el-table-column>
      <el-table-column
        prop="address"
        label="地址">
      </el-table-column>
      <el-table-column
      fixed="right"
      label="点击查看明细"
      width="500">
      <template slot-scope="scope">
        <el-button @click="handleClick(scope.row)" type="text" size="small">进货</el-button>
        <el-button type="text" size="small">退货</el-button>
         <el-button type="text" size="small">付款</el-button>
          <el-button type="text" size="small">总计</el-button>
      </template>
    </el-table-column>
    </el-table>
  </template>
          </el-main>
          <el-footer>版权</el-footer>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
       tableData: [{
            date: '2016-05-02',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }, {
            date: '2016-05-04',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1517 弄'
          }, {
            date: '2016-05-01',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1519 弄'
          }, {
            date: '2016-05-03',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1516 弄'
          }]

    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }, 
     handleClick(row) {
        console.log(row);
      }

  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.myheaderSpan {
  margin-left: -1%;

  height: 60px;
  width: 60px;

  float: left;
  margin-top: -2px;
}
.el-header {
  z-index: 1030;
  margin-bottom: 0;
  border-radius: 0;
  min-height: 60px;
  max-height: 60px;
  background-color: #fff;
  border: 0;
  border-bottom: 1px solid #c9c9c9;
  box-shadow: none;
  background-repeat: repeat-x;
  background-image: -webkit-linear-gradient(top, white 1%, #f3f3f3 100%);
  background-image: linear-gradient(to bottom, #ffffff 1%, #f3f3f3 100%);
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#ffffff', endColorstr='#f3f3f3',GradientType=0);
  filter: progid:DXImageTransform.Microsoft.gradient(enabled=false);
}
.el-footer {
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #e2dede;
  color: #333;
  text-align: left;
  line-height: 200px;
}

.el-main {
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}

.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
}
.bg-purple {
}
.bg-purple-light {
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
}
.glyphicons {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: Glyphicons;
  font-style: normal;
  font-weight: 400;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.navbar-brand {
  height: 60px;
  line-height: 48px;
  padding: 0;
  color: #5d5d5d;
  font-size: 19px;
  font-weight: 400;
  letter-spacing: 0.5px;
}
.myheader {
  text-align: left;
}
.headerWenzi {
  margin-top: 0%;
  float: left;
  height: 60px;
  line-height: 48px;
  padding: 0;
  color: #5d5d5d;
  font-size: 19px;
  font-weight: 400;
  letter-spacing: 0.5px;
}
.myimg {
  width: 60px;
  height: 60px;
}
.myimg2 {
  margin-top: 15%;
  width: 30px;
  height: 30px;
  text-align: center;
  float: right;

  display: table-cell;
  vertical-align: middle;
}
.navbar-menus {
  float: right;
  margin-right: 10px;
}
.navbar-menus > .btn-group {
  float: left;
  margin-right: 0;
}

.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.navbar-menus > .btn-group > button {
  position: relative;
  color: #666;
  padding: 21px 20px 18px;
  background: transparent;
  border: none;
  border-radius: 0;
  outline: none;
}
.glyphicons:empty {
  width: 1em;
}

.myheaderRiget {
  float: right;
  margin-right: 1%;
  width: 5%;
  height: 60px;
}
</style>
