<template>
  <div class="son" style="border:3px solid #000;margin:10px">
    <!-- 3.propsの値を直接使用 -->
    部品Sonです。 {{ title }}
    <button @click="changeFn">修改title</button>
  </div>
</template>

<script>
export default {
  name: 'Son-Child',
  // 2.propsで受け取り
  props: ['title'],
  methods: {
    changeFn() {
      this.$emit('changTitle', '教育')
    }
  }

}
</script>

<style></style>