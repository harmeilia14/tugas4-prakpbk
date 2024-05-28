<template>
  <div id="app">
    <ParentComponent>
      <ChildComponent />
    </ParentComponent>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue'
import ChildComponent from './components/ChildComponent.vue'

export default {
  name: 'App',
  components: {
    ParentComponent,
    ChildComponent // Pastikan untuk menyertakan ChildComponent di sini
  }
}
</script>

<style></style>
