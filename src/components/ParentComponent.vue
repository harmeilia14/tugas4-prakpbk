<template>
  <div class="parent-component">
    <h2 class="title">Komponen Parent</h2>
    <p class="data">Data dari anak: {{ dataFromChild }}</p>
    <child-component @send-data="handleDataFromChild"></child-component>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue'

export default {
  components: {
    ChildComponent
  },
  data() {
    return {
      dataFromChild: ''
    }
  },
  methods: {
    handleDataFromChild(data) {
      this.dataFromChild = data
    }
  }
}
</script>

<style scoped>
.parent-component {
  margin: 20px auto;
  padding: 20px;
  border: 1px solid #5c1a67;
  border-radius: 8px;
  background-color: #962ec3;
  box-shadow: 0 0 10px rgba(250, 164, 254, 0.953);
  text-align: center;
  color: #fff; /* Warna teks putih */
}

.title {
  font-size: 24px;
  margin-bottom: 20px;
}

.data {
  font-size: 16px;
  background-color: #d66ff3;
  padding: 10px;
  border-radius: 5px;
  margin-top: 20px;
}

child-component {
  margin-top: 20px;
}
</style>
