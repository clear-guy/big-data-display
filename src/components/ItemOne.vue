<template>
    <div ref="itemOne" class="itemOne"></div>
</template>

<script setup>
import { inject, ref, onMounted } from 'vue'

let itemOne = ref()

onMounted(() => {
    let $echarts = inject('echarts')
    let myChart = $echarts.init(itemOne.value, 'dark')
    myChart.setOption({
        animationDuration: 5000,
        tooltip: {
            trigger: 'item',
            showDelay: 0,
            transitionDuration: 5
        },
        legend: {
            data: ['白丝', '黑丝', '肉丝', '蕾丝', '渔网']
        },
        xAxis: {
            type: 'category',
            boundaryGap: false,
            data: ['2018年', '2019年', '2020年', '2021年', '2022年', '2023年', '2024年']
        },
        yAxis: {
            type: 'value'
        },
        series: [
            {
                name: '白丝',
                type: 'line',
                data: [1200, 1500, 2000, 1400, 1900, 2220, 2200]
            },
            {
                name: '黑丝',
                type: 'line',
                data: [1220, 1400, 1710, 1500, 2290, 2330, 2310]
            },
            {
                name: '肉丝',
                type: 'line',
                data: [1150, 1310, 1420, 1554, 1790, 1930, 2010]
            },
            {
                name: '蕾丝',
                type: 'line',
                data: [320, 432, 501, 734, 890, 830, 920]
            },
            {
                name: '渔网',
                type: 'line',
                data: [282, 493, 790, 593, 1129, 1133, 2130]
            }
        ]
    })
})
</script>

<style scoped>
.itemOne {
    width: 100%;
    height: 100%;
}
</style>
