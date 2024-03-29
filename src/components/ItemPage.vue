<script setup>
import ItemOne from '@/components/ItemOne.vue'
import ItemTwo from "@/components/ItemTwo.vue"
import ItemThree from "@/components/ItemThree.vue"
import ItemFour from "@/components/ItemFour.vue"
import CenterMap from '@/components/CenterMap.vue'
</script>

<template>
    <div class="item-page">
        <div class="content">
            <div class="left">
                <div class="one">
                    <div class="txt">帅锅丝袜爱好折线图</div>
                    <div class="ione">
                        <ItemOne></ItemOne>
                    </div>
                </div>
                <div class="one">
                    <div class="txt">帅锅丝袜爱好饼状图</div>
                    <div class="ione">
                        <ItemTwo></ItemTwo>
                    </div>
                </div>
            </div>
            <div class="center">
                <div class="two">
                    <div class="txt">帅锅丝袜爱好人数分布图</div>
                    <div class="ione">
                        <CenterMap></CenterMap>
                    </div>
                </div>
            </div>
            <div class="right">
                <div class="one">
                    <div class="txt">帅锅丝袜爱好柱状图</div>
                    <div class="ione">
                        <ItemThree></ItemThree>
                    </div>
                </div>
                <div class="one">
                    <div class="txt">帅锅丝袜爱好饼状图</div>
                    <div class="ione">
                        <ItemFour></ItemFour>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.item-page {
    width: 100%;
    height: 100%;
    color: white;
}

.content {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.left,
.right {
    flex: 3;
    height: 100%;
}

.center {
    flex: 5;
    height: 100%;
}

.one {
    width: 100%;
    height: 50%;
    display: flex;
    flex-direction: column;
}

.two {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
}

.ione {
    flex: 1;
}

.txt {
    text-align: center;
    height: 30px;
    font-weight: 700;
    font-size: 20px;
}
</style>
