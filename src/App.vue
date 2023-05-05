<!-- 主要入口 -->
<script>
import headerVue from "./components/view/HeaderVue.vue";
import cardVue from "./components/view/CardVue.vue";

// <!-- 匯出 -->
export default {
  // <!-- 匯出元件清單 -->
  components: {
    headerVue,
    cardVue
  },
  data() {
    return {
      a: 1,
      temp: 0,
      arr: ["Jhon", "Jenny", "Ariang", "Daddy", "funny"],
      arrMeal: [],
      isShow: true
    }
  },
  methods: {
    changeAValue() {
      this.a = this.temp;
    },
    switchBoo() {
      this.isShow = !this.isShow;
    }
  },
  // 生命週期
  mounted() {

  }
}
</script>

<template>
  <!-- <div>
    <p>Lorem ipsum dolor sit amet.</p>
    <headerVue />
  </div> -->

  <!-- 使用cardVue樣式 -->
  <div>
    <cardVue />
  </div>

  <!-- Vue 指令 - for -->
  <h1>Vue 指令 - for</h1>
  <p>V-for</p>
  <ul>
    <li v-for="item in arr">{{ item }}</li>
  </ul>

  <!-- Vue 指令 - model -->
  <div class="text-area">
    <h1>V-model</h1>
    <h1>V-on</h1>
    <h2>a:{{ a }}</h2>
    <p>temp:{{ temp }}</p>
    <input type="number" v-model="temp">
    <button class="bg-primary" type="button" v-on:click="changeAValue">update</button>
  </div>


  <label for="breackfast">早餐 </label>
  <input id="breackfast" type="checkbox" value="breackfast" v-model="arrMeal">

  <label for="lunch">午餐 </label>
  <input id="lunch" type="checkbox" value="lunch" v-model="arrMeal">

  <label for="dinner">晚餐 </label>
  <input id="dinner" type="checkbox" value="dinner" v-model="arrMeal">

  <!-- 當type是cheackbox時 -->
  <p>{{ arrMeal.join(" ") }}</p>

  <!-- 當type是raido時 -->
  <!-- <p>{{ arrMeal }}</p> -->

  <button type="button" v-on:click="switchBoo">switch</button>
  <p>{{ isShow }}</p>
  <div v-if="isShow" class="box bg-primary"></div>
  <div class="box bg-secondary"></div>
</template>

<style lang="scss">
.text-area {
  text-align: center;
}
</style>