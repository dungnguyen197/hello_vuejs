<template>
  <div>
    <p>Name: {{ user.name }} Email: {{ user.email }}</p>
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
      }
    }
  }
</script>

<style></style>