<template src="./template.html"/>

<script>
    import chatRoom from "@/components/ChatRoom/ChatRoom";

    export default {
        name: "V-Room",
        props:['data','elementIndex'],
        components: {chatRoom}

    }
</script>

<style scoped src="./style.less" lang="less"></style>