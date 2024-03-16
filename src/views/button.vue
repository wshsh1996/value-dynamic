<script setup lang="ts">
import { darkTheme } from 'naive-ui'
import { ref } from 'vue'
import CountTo from '@/components/count-to.vue'

const theme = ref(null)
</script>

<template>
  <n-config-provider :theme="theme">
    <!--  按钮  -->
    <n-card class="about" hoverable>
      <n-space vertical>
        <n-button @click="theme = darkTheme"> 深色 </n-button>
        <n-button @click="theme = null"> 浅色 </n-button>
      </n-space>
    </n-card>
    <!--  格栅  -->
    <n-card class="about2">
      <n-grid :cols="4" :x-gap="40">
        <n-grid-item>
          <div class="light-green">
            <count-to :start-value="1" :end-value="9560"></count-to>
          </div>
        </n-grid-item>
        <n-grid-item>
          <div class="green">2</div>
        </n-grid-item>
        <n-grid-item>
          <div class="light-green">3</div>
        </n-grid-item>
        <n-grid-item>
          <div class="green">4</div>
        </n-grid-item>
      </n-grid>
    </n-card>
   
  </n-config-provider>
</template>

<style scoped>
.about {
  margin: 0 auto 20px;
  width: 1200px;
}
.about2 {
  margin: 0 auto 20px;
  width: 1200px;
}
.about3 {
  margin: 0 auto 20px;
  width: 1200px;
  height: 400px;
  background-color: #f7fafc;
}
.light-green {
  height: 100px;
  background-color: rgba(0, 128, 0, 0.12);
}
.green {
  height: 100px;
  background-color: rgba(0, 128, 0, 0.24);
}
.grid {
  height: 200px;
}
</style>
