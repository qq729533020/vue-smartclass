<template>
  <div id="app">
    <SmartHeader></SmartHeader>
    <main>
      <el-row>
        <el-col :span="3">
          <SmartNav></SmartNav>
        </el-col>
        <el-col :span="21">
          <el-collapse-transition>
            <!-- <transition name="slide-down"> -->
            <keep-alive>
              <router-view></router-view>
            </keep-alive>
          </el-collapse-transition>
          <!-- </transition> -->
        </el-col>
      </el-row>
    </main>
  </div>
</template>

<script>
  import SmartHeader from './components/header.vue'
  import SmartNav from './components/Nav.vue'
  export default {
    components: { //注册组件
      SmartHeader,
      SmartNav
    },
    data() {
      return {
      }
    }
  }

</script>

<style>
  #header {
    line-height: 50px;
    background-color: #20a0ff;
    max-height: 100px;
    min-height: 50px;
    width: 100%;
    border-radius: 4px;
    padding-left: 15px;
    color: #fff;
    box-sizing: border-box;
  }

  #header .el-row {
    margin-bottom: 0;
  }

  .h40,
  .h40 a {
    display: block;
    height: 40px;
    width: 100%;
    line-height: 40px;
  }

  .border2 {
    border: 2px solid #ccc;
  }

  .center {
    text-align: center;
    margin: 0 auto;
  }

  .br5 {
    border-radius: 5px
  }

  .el-row {
    margin-bottom: 20px;
  }

  .slide-down-enter-active,
  .slide-down-leave-active {
    opacity: .2;
    transition: .3s all ease-in;
    transform: translateY(500px);
    /* transform: rotateY(180deg) */
  }

  .slide-down-enter,
  .slide-down-leave {
    opacity: 1;
    transform: translateY(0);
    /* transform: rotateY(0) */
  }
</style>