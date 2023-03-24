<template>
    <img class="img-border" @click="handSrc" :src="src" />
</template>

<script>
import { string } from 'postcss-selector-parser';

export default {
    props:{
        src:string
    },
    methods: {
        handSrc(){
            this.$emit("srcChange",this.src);
        }
    },
}
</script>

<style>
    .img-border{
        border-radius: 40%;
    }
</style>
