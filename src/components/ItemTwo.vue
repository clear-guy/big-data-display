<template>
    <div ref="main" class="main"></div>
</template>

<script setup>
import { onMounted, ref, inject } from 'vue';

let main = ref()
onMounted(() => {
    let $echarts = inject('echarts')
    let myChart = $echarts.init(main.value, 'dark');
    myChart.setOption({
        tooltip: {
            trigger: 'item'
        },
        legend: {
            top: '5%',
            left: 'center'
        },
        series: [
            {
                name: '本年丝袜排名',
                type: 'pie',
                radius: ['40%', '70%'],
                avoidLabelOverlap: false,
                itemStyle: {
                    borderRadius: 10,
                    borderColor: '#fff',
                    borderWidth: 2
                },
                label: {
                    show: false,
                    position: 'center'
                },
                emphasis: {
                    label: {
                        show: true,
                        fontSize: 40,
                        fontWeight: 'bold'
                    }
                },
                labelLine: {
                    show: false
                },
                data: [
                    { value: 2200, name: '白丝' },
                    { value: 2310, name: '黑丝' },
                    { value: 2010, name: '肉丝' },
                    { value: 920, name: '蕾丝' },
                    { value: 2130, name: '渔网' }
                ]
            }
        ]
    })

})
</script>

<style scoped>
.main {
    width: 100%;
    height: 100%;
}
</style>
