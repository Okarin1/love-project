<template>
  <div id="words">
    <div class="text-area">
      <div class="first-textarea">
        <textarea v-model="words" placeholder="请输入任意数字"></textarea>
        <button v-show="words" class="gg-close-o" @click="purgeText()"></button>
      </div>
      <div v-show="words" style="text-align:center">
        <h1 disabled="true" v-text="showWords(words)"></h1>
      </div>
    </div>
  </div>
</template>

<script>
import Toast from "@/common/toast";
import { toLove } from "@/common/love";

export default {
  components: {},
  name: "Words",
  data() {
    return {
      words: null,
    };
  },

  methods: {
    showWords(index) {
      let num = parseInt(index)
      return isNaN(num) ? '' :`${num} = ${toLove(num)}` 
    },
   
    purgeText() {
      this.words = "";
    },
  },
  watch: {
    words() {
      if (this.words === "5201314") {
        setTimeout(
          () => Toast.success("这个就不用论证了吧", 5000),
          1000
        );
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
.text-area {
  margin: 0.5rem;
  display: flex;
  flex-flow: column wrap;
  list-style: none;
}

.text-area textarea {
  margin-top: 20px;
  color: #1f2f3e;
  box-shadow: 1px 1px 2px 0 rgba(0, 0, 0, 0.06);
  border-radius: 5px;
}
.first-textarea {
  display: flex;
  flex-direction: column;
}

.gg-close-o {
  align-self: flex-end;
  margin-right: 15px;
  margin-top: 35px;
  box-sizing: border-box;
  position: absolute;
  display: block;
  transform: scale(var(--ggs, 1));
  width: 22px;
  height: 22px;
  border: 2px solid;
  border-radius: 40px;
  cursor: pointer;
}

.gg-close-o::after,
.gg-close-o::before {
  content: "";
  display: block;
  box-sizing: border-box;
  position: absolute;
  width: 12px;
  height: 2px;
  background: currentColor;
  transform: rotate(45deg);
  border-radius: 5px;
  top: 8px;
  left: 3px;
}

.gg-close-o::after {
  transform: rotate(-45deg);
}

.foo {
  position: relative;
  margin-top: 6vh;
}
</style>
