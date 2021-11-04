<template>
  <HeaderComponent title="Portafolio GH" />
  <FooterComponent />
  <ContainerComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
import ContainerComponent from './components/ContainerComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    FooterComponent,
    ContainerComponent
  }
}
</script>
<style>
@import "../node_modules/bootstrap/dist/css/bootstrap.min.css";

*{
  margin: 0;
  padding: 0;
  font-family: sans-serif;;
}
header{
  width: 100%;
  height: 60px;
  text-align: center;
  background-color: #22577A;
  padding: 0;
  margin: 0;
}
header h1{
  color: white;
  font-size: 25px;
  line-height: 60px;
}
</style>
