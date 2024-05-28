<template>
  <div>
    <h2>Komponen Child</h2>
    <grandchild-component @send-data-to-parent="sendDataToParent"></grandchild-component>
  </div>
</template>

<script>
import GrandchildComponent from './GrandchildComponent.vue'

export default {
  components: {
    GrandchildComponent
  },
  methods: {
    sendDataToParent(data) {
      this.$emit('send-data', data)
    }
  }
}
</script>

<style scoped>
/* Your styles here */
</style>
