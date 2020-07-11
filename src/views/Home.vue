<!--  -->
<template>
  <div class="container">
    <header>
      <div class="area">一楼内科候诊区</div>
      <div class="date">2020年7月10日 15:13 星期五</div>
    </header>
    <div class="up">
      <div class="call-message" v-for="(item, index) in contents" :key="index">{{item}}</div>
    </div>
    <div class="down">
      <el-carousel direction="vertical" indicator-position="none" :interval="5000">
        <el-carousel-item v-for="item in 3" :key="item">
          <div class="card-table">
            <div class="col">
              <div class="table">
                <h2>科室一诊室</h2>
                <div class="pop">占位</div>
                <div class="price">
                  <span>占位</span>
                </div>
                <ul>
                  <li>
                    <strong>A001</strong>周杰伦
                  </li>
                  <li>
                    <strong>A002</strong>林书豪
                  </li>
                  <li>
                    <strong>A003</strong>张学友
                  </li>
                  <li>
                    <strong>A004</strong>张国荣
                  </li>
                </ul>
              </div>
            </div>
            <div class="col">
              <div class="table">
                <h2>科室一诊室</h2>
                <div class="pop">占位</div>
                <div class="price">
                  <span>占位</span>
                </div>
                <ul>
                  <li>
                    <strong>A001</strong>周杰伦
                  </li>
                  <li>
                    <strong>A002</strong>林书豪
                  </li>
                  <li>
                    <strong>A003</strong>张学友
                  </li>
                  <li>
                    <strong>A004</strong>张国荣
                  </li>
                </ul>
              </div>
            </div>
            <div class="col">
              <div class="table">
                <h2>科室一诊室</h2>
                <div class="pop">占位</div>
                <div class="price">
                  <span>占位</span>
                </div>
                <ul>
                  <li>
                    <strong>A001</strong>周杰伦
                  </li>
                  <li>
                    <strong>A002</strong>林书豪
                  </li>
                  <li>
                    <strong>A003</strong>张学友
                  </li>
                  <li>
                    <strong>A004</strong>张国荣
                  </li>
                </ul>
              </div>
            </div>
            <div class="col">
              <div class="table">
                <h2>科室一诊室</h2>
                <div class="pop">占位</div>
                <div class="price">
                  <span>占位</span>
                </div>
                <ul>
                  <li>
                    <strong>A001</strong>周杰伦
                  </li>
                  <li>
                    <strong>A002</strong>林书豪
                  </li>
                  <li>
                    <strong>A003</strong>张学友
                  </li>
                  <li>
                    <strong>A004</strong>张国荣
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
//这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//例如：import 《组件名称》 from '《组件路径》';

export default {
  //import引入的组件需要注入到对象中才能使用
  components: {},
  data() {
    //这里存放数据
    return {
      contents: ['请张三丰到内科一诊室就诊', '请张无忌到内科一诊室就诊', '请令狐冲到内科一诊室就诊']
    }
  },
  //接收父组件数据
  props: {},
  //监听属性 类似于data概念
  computed: {},
  //监控data中的数据变化
  watch: {},
  //方法集合
  methods: {

  },
  //生命周期 - 创建完成（可以访问当前this实例）
  created() {

  },
  //生命周期 - 挂载完成（可以访问DOM元素）
  mounted() {

  },
  beforeCreate() { }, //生命周期 - 创建之前
  beforeMount() { }, //生命周期 - 挂载之前
  beforeUpdate() { }, //生命周期 - 更新之前
  updated() { }, //生命周期 - 更新之后
  beforeDestroy() { }, //生命周期 - 销毁之前
  destroyed() { }, //生命周期 - 销毁完成
  activated() { }, //如果页面有keep-alive缓存功能，这个函数会触发
}
</script>
<style scoped>
.container {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
}
header {
  width: 100%;
  height: 35px;
  background-color: beige;
  display: flex;
  text-align: center;
  line-height: 35px;
}

header .area {
  flex: 1;
  font-size: 25px;
  background: #b3c0d1;
}
header .date {
  flex: 0.4;
  font-size: 14px;
  background-color: beige;
}

.up {
  font-size: 14px;
  top: 35px;
  bottom: 60vh;
  left: 0;
  right: 0;
  overflow: hidden;
  position: absolute;
  border: 2px solid #eee;
  text-align: center;
}
.up .call-message {
  margin: 10px auto;
  height: 26.5px;
  width: 560px;
  line-height: 26.5px;
  background-color: #eee;
  border-radius: 5px;
  box-shadow: 10px 10px 15px rgba(0, 0, 0, 0.5);
}

.down {
  font-size: 25px;
  height: 60vh;
  left: 0;
  right: 0;
  bottom: 0;
  position: fixed;
  background-color: #b3c0d1;
  overflow: hidden;
}

.card-table {
  max-width: 100%;
  margin: auto;
  display: flex;
  justify-content: center;
  text-align: center;
  flex-wrap: wrap;
}

.col {
  flex: 25%;
  padding: 10px;
  max-width: 25%;
  box-sizing: border-box;
}

.table {
  background-color: beige;
  padding: 0 5px;
  font-family: 'montserrat', sans-serif;
  position: relative;
  overflow: hidden;
  box-shadow: 0 0 10px #00000070;
  font-size: 14px;
  height: 55vh;
}

.table ul {
  margin: 0;
  padding: 0;
}

.table ul li {
  padding: 5px 0;
  list-style: none;
}

.price span {
  display: block;
  font-size: 14px;
}

.pop {
  font-size: 10px;
  background: #2c3e50;
  color: #fff;
  transform: rotate(45deg);
  padding: 5px 40px;
  position: absolute;
  top: 5px;
  right: -34px;
}
</style>