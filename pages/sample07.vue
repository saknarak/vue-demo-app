<template>
  <div>
    <h1>Hello {{name}}</h1>
    <input type="text" v-model="code">
    <input type="text" v-model="name">
    <button @click="addStudent">Add</button>
    <ul>
      <li class="big" :class="{red: st.name.length <= 3}" v-for="st in student" :key="st.code">
        {{st.code}} {{st.name}}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      code: '',
      name: 'Somsak',
      student: [
        { code: '001', name: 'Name1' },
        { code: '002', name: 'Name2' },
        { code: '003', name: 'Name3' },
        { code: '004', name: 'Name4' },
      ],
    }
  }, // data
  methods: {
    addStudent() {
      this.student.push({
        code: this.code,
        name: this.name,
      })
    },
  }, // methods
}
</script>
<style scoped>
.big {
  font-size: 16px;
}
.red {
  color: red;
}
</style>
