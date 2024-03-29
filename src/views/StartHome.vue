<script setup>
import ItemPage from '@/components/ItemPage.vue'
</script>

<template>
    <div class="home">
        <!-- title -->
        <div class="title">
            <div>优雅男士丝袜鉴赏</div>
        </div>
        <!-- main -->
        <div class="main">
            <ItemPage></ItemPage>
        </div>
    </div>
</template>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.home {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 1);
}

.title {
    color: white;
    font-size: 28px;
    font-weight: 900;
    width: 100%;
    flex: 1;
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.main {
    width: 100%;
    flex: 6;
}
</style>
