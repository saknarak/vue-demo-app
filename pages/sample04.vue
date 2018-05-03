<template>
  <div>
    <h1>{{age}}Hello {{name}}</h1>
    <h2>{{upperName}}</h2>
    <input type="text" :value="name"><br>
    <input type="text" v-model="name"><br>
    <input type="text" v-model="name"><br>
    <v-btn @click="doSave"><v-icon>favorite</v-icon> SAVE</v-btn>
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
  methods: {
    doSave() {
      this.checkForm()
      console.log('save', this.name, this.upperName)
    },
    checkForm() {

    },
  },
}
</script>
