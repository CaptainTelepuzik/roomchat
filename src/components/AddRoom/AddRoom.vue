<template src="./template.html"/>

<script>
    export default {
        name: "V-AddRoom",
        props: ['indexRoom'],
        beforeMount() {
            this.room = {...this.defaultRoom}
        },
        data() {
            return {
                room: null,
                defaultRoom: {
                    title: ""
                }
            }
        },
        methods: {
            closeForm() {
              this.room = null;
              this.$emit('close');
            },
            addRoom() {
                this.$emit('addRoom', {id: this.indexRoom, ...this.room});
                this.room = null;
                this.closeForm()
            }
        }
    }

</script>

<style scoped src="./style.less" lang="less"></style>