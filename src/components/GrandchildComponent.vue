<template>
    <div>
      <button @click="sendData">Send Data to Child</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'GrandchildComponent',
    methods: {
      sendData() {
        this.$emit('data-from-grandchild', 'Data from Grandchild');
      }
    }
  }
  </script>
  