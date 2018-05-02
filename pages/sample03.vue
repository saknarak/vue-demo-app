<template>
  <div>
    <h1>{{age}}Hello {{name}}</h1>
    <h2>{{upperName}}</h2>
    <input type="text" :value="name"><br>
    <input type="text" v-model="name"><br>
    <input type="text" v-model="name">
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: 'Somsak',
      age: 25,
      salary: 100000,
    }
  },
  computed: {
    upperName() {
      return this.name.toUpperCase()
    },
  },
}
</script>
