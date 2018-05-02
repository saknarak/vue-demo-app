<template>
  <div>
    <h1>{{age}}Hello {{name}}</h1>
    <input type="text" :value="name"><br>
    <input type="text" v-model="name"><br>
    <input type="text" v-model="name">
  </div>
</template>
<script>
export default {
  data() {
    // setInterval(() => {
    //   this.name += '*'
    // }, 3000)

    return {
      name: 'Somsak',
      age: 25,
    }
  },
}
</script>
