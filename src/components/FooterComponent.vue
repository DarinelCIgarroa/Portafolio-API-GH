<template>
  <footer>
    <h3>Darinel Cigarroa De Los Santos &copy;  {{ new Date().getFullYear() }}</h3>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #38A3A5;
  padding: 10px;
  text-align: center;
}
footer h3 {
  color: #000000;
  font-size: 1rem;
}
</style>