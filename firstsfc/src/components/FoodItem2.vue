<template>
  <div class="labanos">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Patatas and labanos',
      message: 'I like Patatas and labanos'
    }
  }
};
</script>

<style>
.labanos {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: rgb(208, 20, 255);
  }
</style>