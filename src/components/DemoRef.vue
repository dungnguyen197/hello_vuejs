<template>
    <div class="demo-ref">
        <h1>DemoRef</h1>
        <button class="avatar" v-on:click="handleClickInputFile">Thay đổi avatar</button>
        <input ref="fileInputAvatar" type="file" style="display: none" multiple>
    </div>
</template>

<script>
    export default {
        name: 'demo-ref',
        data() {
            return {

            }
        },
        methods: {
            handleClickInputFile() {
               this.$refs.fileInputAvatar.click();
            }
        }
    }
</script>

<style>
    .demo-ref {
        margin-top: 10px;
        padding: 100px 30px;
        border: 1px solid;
    }
    .avatar {
        color: #FFF;
        border: 2px solid #333;
        padding: 12px 15px;
        background-color: #333;
        transition: all .3s ease;
    }
    .avatar:hover {
        color: #333333;
        background-color: #FFFFFF;
    }
</style>