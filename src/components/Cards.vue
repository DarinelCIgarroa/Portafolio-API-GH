<template>
  <div class="cards">
    <div class="card-title">
      <h3>{{ name }}</h3>
    </div>
    <div class="card-body">
      <p>
        {{ description }}
      </p>
    </div>
    <div class="card-footer">
      <p>{{ created_at }}</p>
      <ButtonComponent
        :url_redirect="url_repository"
        color="dark"
      />
      <ButtonComponent
        v-show="url_homePage != null"  
        :url_redirect="url_homePage"
        color="red"
        title="Ir a la pagina"
      />
    </div>
  </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";
export default {
  name: "Cards",
  components: { ButtonComponent },
  props: {
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    created_at: {
      type: String,
      required: true,
    },
    url_repository: {
      type: String
    },
    url_homePage: {
      type: String,
    }
  },
};
</script>

<style scoped>
.cards {
  width: 300px;
  min-width: 250px;
  min-height: 120px;
  margin: 5px;
  border: solid 0.5px black;
}
.card-title {
  padding: 5px;
  border-bottom: 1px solid black;
}
.card-body {
  padding: 5px;
  border-bottom: 1px solid black;
}
.card-footer {
  padding: 5px;
}
</style>
