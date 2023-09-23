<template>
  <div class="app" style="border: 3px solid #000; margin: 10px">
    <baseCount></baseCount>
    <baseCount></baseCount>
    <baseCount></baseCount>
    <br>
    <!-- 1｡タグに属性追加し値を渡す -->
    <Son :title="myTitle" @changTitle="handleChange"></Son>
    <br>
    <UserInfo :style="{ margin: '0 10px' }" :username="username" :age="age" :isSingle="isSingle" :car="car"
      :hobby="hobby">
    </UserInfo>
    <br><br>
    <BaseProgress :style="{ margin: '0 10px' }" :w="width"></BaseProgress>
    <br>
    <br>
    <base-count01 :count="count" @changeCount="handleChange01"></base-count01>
    <br>
  </div>
</template>

<script>
import baseCount from './components/BaseCount'
import UserInfo from './components/UserInfo.vue'
import Son from "./components/Son.vue"
import BaseProgress from "./components/BaseProgress.vue"
import BaseCount from './components/BaseCount.vue'
import BaseCount01 from './components/BaseCount01.vue'

export default {
  components: {
    baseCount,
    UserInfo,
    BaseProgress,
    Son,
    BaseCount,
    BaseCount01
  },
  data() {
    return {
      myTitle: '私はフロントエンジニアです。',
      username: '小帅',
      age: 28,
      isSingle: true,
      car: {
        brand: '宝马',
      },
      hobby: ['篮球', '足球', '羽毛球'],
      width: 10,

      count: 10
    }
  },
  methods: {
    handleChange(newValue) {
      console.log(newValue);
      this.myTitle = newValue
    },

    handleChange01(newVal) {
      console.log(newVal)
      this.count = newVal
    }
  }
}
</script>

<style></style>
