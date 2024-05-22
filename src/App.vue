<template>
  <div id="app">
    <parent-component>
      <template v-slot>
        <p>ini adalah konten tambahan pada slot parent component</p>
      </template>
    </parent-component>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  name: 'App',
  components: {
    ParentComponent
  }
}
</script>
