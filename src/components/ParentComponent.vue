<template>
    <div>
      <p>Parent Component Received: {{ receivedData }}</p>
      <child-component @data-from-child="receiveDataFromChild"></child-component>
      <slot></slot>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: 'ParentComponent',
    components: {
      ChildComponent
    },
    data() {
      return {
        receivedData: ''
      }
    },
    methods: {
      receiveDataFromChild(data) {
        this.receivedData = `${data}`;
      }
    }
  }
  </script>
  