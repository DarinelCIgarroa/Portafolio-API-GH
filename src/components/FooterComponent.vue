<template>
  <footer>
    <h3>
      Darinel Cigarroa De Los Santos &copy; {{ new Date().getFullYear() }}
    </h3>
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
  height: 50px;
  width: 100%;
  bottom: 0;
  background-color: #38a3a5;
  text-align: center;
}
footer h3 {
  color: #000000;
  line-height: 50px;
  font-size: 1rem;
}
</style>