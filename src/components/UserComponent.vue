<template>
  <div>
    <p>Name: {{ user.name }} Email: {{ user.email }} <button v-on:click="deleteUser">Delete</button></p>
  </div>
</template>

<script>
  export default {
    name: 'user-component',
    data() {
      return {
       
      }
    },
    props: {
      user: {
        type: Object,
        default: {}
      },

    },
    methods: {
      deleteUser() {
          let index = this.$vnode.key;
          this.$emit('deleteUser', {index: index});
      }
    }
  }
</script>

<style></style>