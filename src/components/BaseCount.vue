<template>
      <div class="base-count">
            <button @click="count--">-</button>
            <span>{{ count }}</span>
            <button @click="count++">+</button>
      </div>
</template>
    
<script>
export default {
      data: function () {
            return {
                  count: 100,
            }
      },
}
</script>
    
<style>
.base-count {
      margin: 20px;
}
</style>