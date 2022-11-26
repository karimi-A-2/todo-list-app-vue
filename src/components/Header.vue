<template>
  <header>
    <h1>{{title}}</h1>
  </header>
</template>

<script>
export default {
  name: "Header",
// method 1: using array ==>
//   props: ['title'],

// method 2: using object with title and type 
//   props: {
//     title: String,
//   },

// method 3: also specifying default value
  props: {
    title: {
        tyepe: String,
        default: 'Hello World',
    },
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>