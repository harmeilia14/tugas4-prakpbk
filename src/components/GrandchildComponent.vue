<template>
  <div>
    <button @click="sendData" style="background-color: #33053f; color: #fff">
      Tampilkan data di halaman parent
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    sendData() {
      const data = 'Saya Harmeilia Reski Rahmayani!'
      this.$emit('send-data-to-parent', data)
    }
  }
}
</script>

<style scoped>
/* Your styles here */
</style>
