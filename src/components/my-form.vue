<template>
    <view>
        <view class="title">标题</view>
        <view class="content">
            <span>内容</span>
            <slot></slot>
        </view>
    </view>
</template>

<script>

export default {
    mounted(){
        console.log("组件加载完毕！");
    }
}
</script>

<style>
</style>
