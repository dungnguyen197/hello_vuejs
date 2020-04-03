<template>
  <div>
    <h2>List User Component</h2>
    <user-component 
      v-for="(user, index) in listUser" 
      v-bind:key="index" 
      v-bind:user="user"
      v-on:deleteUser="deleteUser" />
  </div>
</template>

<script>
  import UserComponent from './UserComponent.vue'

  export default {
    name: 'list-user-component',
    data() {
      return {
       
      }
    },
    components: {
      UserComponent
    },
    props: {
      listUser: {
        type: Array,
        default: []
      }
    },
    methods: {
      deleteUser(index) {
        this.$emit('deleteUser', index);
      }
    }
  }
</script>

<style>

</style>