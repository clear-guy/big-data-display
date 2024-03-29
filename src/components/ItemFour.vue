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

            legend: {
                data: ['白丝', '黑丝', '肉丝', '蕾丝', '渔网']
            },
            radar: {
                // shape: 'circle',
                indicator: [
                    { name: '性感', max: 20000 },
                    { name: '乖巧', max: 20000 },
                    { name: '诱人', max: 20000 },
                    { name: '火辣', max: 20000 },
                    { name: '难看', max: 20000 },
                    { name: '可爱', max: 20000 }
                ]
            },
            series: [
                {
                    name: 'Budget vs spending',
                    type: 'radar',
                    tooltip: {
                        trigger: 'item'
                    },
                    data: [
                        {
                            value: [14000, 20000, 18000, 10000, 0, 20000],
                            name: '白丝'
                        },
                        {
                            value: [20000, 10000, 20000, 20000, 0, 10000],
                            name: '黑丝'
                        },
                        {
                            value: [15000, 10000, 8000, 9000, 5000, 12000],
                            name: '肉丝'
                        },
                        {
                            value: [18000, 12000, 17000, 10000, 1000, 15000],
                            name: '蕾丝'
                        },
                        {
                            value: [17000, 4000, 20000, 16000, 2000, 9000],
                            name: '渔网'
                        }
                    ]
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
