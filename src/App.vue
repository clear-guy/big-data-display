<script setup>
import { provide } from 'vue';
import * as echarts from 'echarts';

import dark from './assets/dark.json';
provide('echarts', echarts)
echarts.registerTheme('dark', dark);
</script>

<template>
  <header>
    <div class="wrapper">
      <RouterLink to="/"></RouterLink>
    </div>
  </header>

  <RouterView />
</template>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
