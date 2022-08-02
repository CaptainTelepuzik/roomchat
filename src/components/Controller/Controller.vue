<template src="./template.html"/>

<script>


    import AddRoom from "@/components/AddRoom/AddRoom";
    import RegistrRoom from "@/components/RegistrRoom/RegistrRoom";
    import Room from "@/components/Room/Room";

    export default {
        name: "V-Controller",
        components: {
            AddRoom, RegistrRoom, Room,
        },
        data() {
            return {
                rooms: [{
                    title: "",
                    message: [],
                }],
                addFormVisible: false,
                addRoomVisible: false,
                indexRoom: 0
            }
        },
        methods: {
            closeAddRoom() {
                this.addFormVisible = false;
            },

            AddRoom(roomData) {
                this.indexRoom++
                this.rooms.push(roomData)
            },
            addButtonClick() {
                this.addFormVisible = true;
            },
            addButtonRoom() {
            this.addRoomVisible = true;
          }
        }
    }
</script>

<style scoped src="./style.less" lang="less"></style>