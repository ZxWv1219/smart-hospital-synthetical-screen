<!--  -->
<template>
  <div id="box">
    <div id="login-box">
      <h1>欢迎登录</h1>
      <div class="form">
        <div class="item">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-User" />
          </svg>
          <input type="text" placeholder="用户名" />
        </div>
        <div class="item">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-password" />
          </svg>
          <input type="text" placeholder="密码" />
        </div>
      </div>
      <a id="btn" @click="btnListener">登录</a>
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
      btn: null
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
    btnListener(e) {
      let btn = document.getElementById('btn')
      let x = e.clientX - e.target.offsetLeft
      let y = e.clientY - e.target.offsetTop
      let span = document.createElement('span')
      span.style.left = x + 'px'
      span.style.top = y + 'px'
      btn.appendChild(span)
      setTimeout(function () {
        span.remove()
      }, 500)
    }
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
<style>
#box {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('~@/assets/img/login/lz.jpg');
  background-repeat: 'no-repeat';
  background-size: 100% auto;
}
#login-box {
  width: 30%;
  height: auto;
  margin: 0 auto;
  margin-top: 15%;
  text-align: center;
  background: #00000080;
  padding: 20px 50px;
}
#login-box h1 {
  color: #fff;
}
#login-box .form .item {
  margin-top: 15px;
}

#login-box .form .item svg {
  font-size: 15px;
  color: #fff;
}

#login-box .form .item input {
  width: 150px;
  font-size: 13px;
  border: 0;
  border-bottom: 1.5px solid #fff;
  padding: 5px 10px;
  background: #ffffff00;
  color: #fff;
  outline: medium;
}

#login-box a {
  position: relative;
  display: inline-block;
  padding: 5px 36px;
  margin-top: 25px;
  color: #ffffff;
  font-size: 14px;
  letter-spacing: 2px;
  border-radius: 40px;
  background-image: linear-gradient(-225deg, #20e2d7 0%, #f9fea5 100%);
  overflow: hidden;
  cursor: pointer;
  user-select: none;
}

#login-box a span {
  position: absolute;
  background-color: #fff;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  animation: ani 0.5s linear infinite;
  pointer-events: none;
}

@keyframes ani {
  0% {
    width: 0;
    height: 0;
    opacity: 0.5s;
  }
  100% {
    width: 500px;
    height: 500px;
    opacity: 0;
  }
}
</style>