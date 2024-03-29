<template>
    <div ref="main" class="main"></div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import * as echarts from 'echarts';
import china from '../assets/china.json'
echarts.registerMap("china", china);
let main = ref()
onMounted(() => {
    // let $echarts = inject('echarts')
    let myChart = echarts.init(main.value, 'dark');
    myChart.setOption(
        {
            tooltip: {
                trigger: "item",
            },
            visualMap: {
                left: "right",
                min: 0,
                max: 1000,
                color: 'white',
                inRange: {
                    color: [
                        "#313695",
                        "#4575b4",
                        "#74add1",
                        "#abd9e9",
                        "#e0f3f8",
                        "#ffffbf",
                        "#fee090",
                        "#fdae61",
                        "#f46d43",
                        "#d73027",
                        "#a50026",
                    ],
                },
                text: ["最高", "最低"],
                textStyle: {
                    color: 'white'
                },
                calculable: true,
            },
            series: [
                {
                    type: "map",
                    map: "china", // 引入地图数据
                    name: "优雅男士喜欢丝袜人数（单位：万人）",
                    data: [
                        {
                            name: "北京市",
                            value: 510,
                            color: 'white'
                        },
                        {
                            name: "天津市",
                            value: 600,
                        },
                        {
                            name: "上海市",
                            value: 799,
                        },
                        {
                            name: "重庆市",
                            value: 980,
                            color: 'white'
                        },
                        {
                            name: "河北省",
                            value: 700,
                            color: 'white'
                        },
                        {
                            name: "河南省",
                            value: 590,
                        },
                        {
                            name: "云南省",
                            value: 779,
                        },
                        {
                            name: "辽宁省",
                            value: 380,
                        },
                        {
                            name: "黑龙江省",
                            value: 391,
                        },
                        {
                            name: "湖南省",
                            value: 720,
                        },
                        {
                            name: "安徽省",
                            value: 584,
                        },
                        {
                            name: "山东省",
                            value: 572,
                        },
                        {
                            name: "新疆维吾尔自治区",
                            value: 289,
                        },
                        {
                            name: "江苏省",
                            value: 770,
                        },
                        {
                            name: "浙江省",
                            value: 585,
                        },
                        {
                            name: "江西省",
                            value: 511,
                        },
                        {
                            name: "湖北省",
                            value: 662,
                        },
                        {
                            name: "广西壮族自治区",
                            value: 813,
                        },
                        {
                            name: "甘肃省",
                            value: 474,
                        },
                        {
                            name: "山西省",
                            value: 378,
                        },
                        {
                            name: "内蒙古自治区",
                            value: 174,
                        },
                        {
                            name: "陕西省",
                            value: 400,
                        },
                        {
                            name: "吉林省",
                            value: 399,
                        },
                        {
                            name: "福建省",
                            value: 490,
                        },
                        {
                            name: "贵州省",
                            value: 999,
                        },
                        {
                            name: "广东省",
                            value: 621,
                        },
                        {
                            name: "青海省",
                            value: 520,
                        },
                        {
                            name: "西藏自治区",
                            value: 210,
                        },
                        {
                            name: "四川省",
                            value: 998,
                        },
                        {
                            name: "宁夏回族自治区",
                            value: 111,
                        },
                        {
                            name: "海南省",
                            value: 425,
                        },
                        {
                            name: "台湾省",
                            value: 816,
                        },
                        {
                            name: "香港特别行政区",
                            value: 888,
                        },
                        {
                            name: "澳门特别行政区",
                            value: 950,
                        },
                    ],
                    itemStyle: {
                        emphasis: {
                            // 高亮状态
                            label: {
                                color: 'white'
                            }
                        }
                    }
                },
            ],
        })
})
</script>

<style scoped>
.main {
    width: 100%;
    height: 100%;
    color: white;
}
</style>
