<template>
    <view>
        <my-form>
            <view>
                <input class="input" placeholder="请输入" />
                <radio class="radio"></radio>
                <checkbox class="checkbox"></checkbox>
            </view>
        </my-form>
    </view>
</template>
 
<script>
import myForm from '@/components/my-form'
export default {
    components: {
        myForm
    },
    onShow(){
        console.log("页面显示!");
    },
    onLoad(){
        console.log("页面加载完毕");
    }
}
</script>
<style>
</style>
 