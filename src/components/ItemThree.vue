<template>
    <div ref="main" class="main"></div>
</template>

<script setup>
import { onMounted, ref, inject } from 'vue';
let main = ref()
onMounted(() => {
    let $echarts = inject('echarts')
    let myChart = $echarts.init(main.value, 'dark');
    myChart.setOption(
        {
            xAxis: {
                data: ['白丝', '黑丝', '肉丝', '蕾丝', '渔网'],
                axisLabel: {
                    inside: true,
                    color: '#fff'
                },
                axisTick: {
                    show: false
                },
                axisLine: {
                    show: false
                },
                z: 10
            },
            yAxis: {
                axisLine: {
                    show: false
                },
                axisTick: {
                    show: false
                },
                axisLabel: {
                    color: '#999'
                }
            },
            dataZoom: [
                {
                    type: 'inside'
                }
            ],
            series: [
                {
                    type: 'bar',
                    showBackground: true,
                    itemStyle: {
                        color: new $echarts.graphic.LinearGradient(0, 0, 0, 1, [
                            { offset: 0, color: '#83bff6' },
                            { offset: 0.5, color: '#188df0' },
                            { offset: 1, color: '#188df0' }
                        ])
                    },
                    emphasis: {
                        itemStyle: {
                            color: new $echarts.graphic.LinearGradient(0, 0, 0, 1, [
                                { offset: 0, color: '#2378f7' },
                                { offset: 0.7, color: '#2378f7' },
                                { offset: 1, color: '#83bff6' }
                            ])
                        }
                    },
                    data: [{ value: 2200, itemStyle: { color: '#ae56f9' } },
                    { value: 2310, itemStyle: { color: '#00dcff' } },
                    { value: 2010, itemStyle: { color: '#f2ae99' } },
                    { value: 920, itemStyle: { color: '#00ff85' } },
                    { value: 2130, itemStyle: { color: '#ff4c00' } }]
                }
            ]
        }
    )
})
</script>

<style scoped>
.main {
    width: 100%;
    height: 100%;
}
</style>
