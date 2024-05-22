<template>
    <div>
      <p>Child Component Received: {{ receivedData }}</p>
      <grandchild-component @data-from-grandchild="receiveDataFromGrandchild"></grandchild-component>
    </div>
  </template>
  
  <script>
  import GrandchildComponent from './GrandchildComponent.vue';
  
  export default {
    name: 'ChildComponent',
    components: {
      GrandchildComponent
    },
    data() {
      return {
        receivedData: ''
      }
    },
    methods: {
      receiveDataFromGrandchild(data) {
        this.receivedData = `${data}`;
        this.$emit('data-from-child', `${data}`);
      }
    }
  }
  </script>
  