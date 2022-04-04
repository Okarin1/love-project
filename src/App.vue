<template>
  <div id="app">

    <div class="content-box">
          <words />
      
      
      <h2>说明</h2>
      <p>二改自波波口老师的
       <a href="https://github.com/itorr/homo" target="_blank"
       >恶臭数字论证器</a
        >
      </p>

      <h2>打赏</h2>
      <p>
       <a href="https://donate.okarin.cn/" target="_blank"
          >点击这里请我喝瓶美汁源吧！</a
        >
      </p>

      <h2>仓库地址</h2>
      <p>
        <a href="https://github.com/Okarin1/love-project" target="_blank"
          >https://github.com/Okarin1/love-project</a
        >
      </p>

      <h2>鸣谢</h2>
      <p>💗亲爱的波波口老师 <a href="https://weibo.com/reiove" target="_blank">@卜卜口</a></p>

      <div class="footer">
        MIT Licensed | Copyright © 2022-present <a href="https://weibo.com/u/6331216566" target="_blank">@Okarin</a>
      </div>
    </div>
  </div>
</template>

<script>
import Words from "./components/Words.vue";

export default {
  name: "App",
  components: {
    Words,
  },
};
</script>

<style lang="less">
@import "assets/css/base.css";
@import "assets/css/okarin.less";

.cpt-toast {
  position: fixed;
  right: 0;
  left: 0;
  bottom: 20vh;
  text-align: center;
}
.success {
  font-size: 15px;
  color: white;
  padding: 10px;
  border-radius: 30px;
  background-color: rgba(14, 13, 13, 0.6);
}
</style>

