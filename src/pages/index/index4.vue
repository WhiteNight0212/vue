<template>
    <view>
        <view v-show="src != null && src.length != 0">图片地址：{{ src }}</view>
        <imgBorder @srcChange="getSrc" :src="src1"></imgBorder>
        <img-border @srcChange="getSrc" :src="src2"></img-border>
    </view>
</template>
 
<script>
import imgBorder from '@/components/img-border'
export default {
    data() {
        return {
            src: "",
            src1: "https://bkimg.cdn.bcebos.com/pic/4a36acaf2edda3cc17c872980fe93901213f925e",
            src2: "https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201912%2F13%2F20191213231738_mmkco.thumb.1000_0.jpg&refer=http%3A%2F%2Fc-ssl.duitang.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1682146567&t=2f6d1ee68fd76cf1ee66f78df5cc2e40"
        }
    },
    components: {
        imgBorder: imgBorder
    },
    methods: {
        getSrc(p) {
            console.log(p);
            this.src = p;
        }
    },
    onLoad() {
        console.log(this.baseUrl);
        console.log(getApp().globalData.baseUrl2);
    }
}
</script>
 
<style></style>
 