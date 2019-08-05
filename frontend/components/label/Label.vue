<template>
    <a class="link" target="_blank" :href="link.href">
        <span class="name">{{ link.name }}</span>
        <img :src="link.img" :alt="link.name">
    </a>
</template>
<script>
export default {
    name: 'Label',
    props: {
        link: {
            type: Object,
            default: () => {}
        }
    }
    
}
</script>
<style lang="scss" scoped>
.link {
    width: 300px;
    display: block;
    height: 80px;
    box-sizing: border-box;
    border: 1px solid #ececec;
    padding: 10px 20px;
    background: #fff;
    margin-bottom: 40px;
    &::after {
        content: "";
        display: block;
        height: 0;
        clear: both;
    }
    .name {
        float: left;
        font-size: 14px;
        color: #333;
        line-height: 58px;
        width: calc(100% - 58px);
    }
    img {
        float: right;
        width: 58px;
        height: 58px;
        border: 1px solid #ececec;
        border-radius: 10px;
    }
}
</style>
