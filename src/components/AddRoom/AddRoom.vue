<template src="./template.html"/>

<script>
    export default {
        name: "V-AddRoom",
        props: ['indexTask'],
        beforeMount() {
            this.room = {...this.defaultRoom}
        },
        data() {
            return {
                room: null,
                defaultRoom: {
                    title: "",
                    message: []
                }
            }
        },
        methods: {
            closeForm() {
                this.$emit('close');
            },
            addRoom() {
                this.$emit('addRoom', {id: this.indexRoom, ...this.room});
                this.closeForm()
            }
        }
    }

</script>

<style scoped src="./style.less" lang="less"></style>