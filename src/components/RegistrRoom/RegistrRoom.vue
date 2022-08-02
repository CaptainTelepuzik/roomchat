<template src="./template.html"/>
<script>

import Room from "@/components/Room/Room";

    export default {
      name: "V-RegistrRoom",
      props: ["elementIndex", "data"],
      components: {Room},
      methods:{
        addButtonClick(){
          this.$emit('addButtonClick');
        },
        addButtonRoom(){
          this.$emit('addButtonRoom');
        }
      }
    }
</script>

<style scoped src="./style.less" lang="less"></style>