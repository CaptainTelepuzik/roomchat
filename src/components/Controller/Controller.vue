<template src="./template.html"/>

<script>


    import AddRoom from "@/components/AddRoom/AddRoom";
    import RegistrRoom from "@/components/RegistrRoom/RegistrRoom";
    import ChatRoom from "@/components/ChatRoom/ChatRoom";

    export default {
        name: "V-Controller",
        components: {
            AddRoom, RegistrRoom, ChatRoom
        },
        data() {
            return {
                rooms: [{
                    title: "",
                    message: []
                }],
                addFormVisible: false,
                indexTask: 0
            }
        },
        methods: {
            closeAddRoom() {
                this.addFormVisible = false;
            },

            AddRoom() {
                this.addFormVisible = true;
            },
            addButtonClick() {
                this.addFormVisible = true;

            }
        }
    }
</script>

<style scoped src="./style.less" lang="less"></style>