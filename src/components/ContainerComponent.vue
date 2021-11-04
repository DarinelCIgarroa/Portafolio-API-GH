<template>
  <div class="container mb-6">
    <h2>Mis proyectos</h2>
    <hr />
    <LoaderComponent v-show="loader" />
    <div class="cards-item">
      <div class="content-card" v-for="project in projects" :key="project.id">
        <Cards
          :name="project.name"
          :description="project.description"
          :url_homePage="project.homepage"
          :url_repository="project.html_url"
          :created_at="project.created_at"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Cards from "./Cards.vue";
import LoaderComponent from "./LoaderComponent.vue";
export default {
  name: "ContainerComponent",
  components: { Cards, LoaderComponent },
  mounted() {
    this.getProjects();
  },
  methods: {
    async getProjects() {
      const response = await fetch(
        "https://api.github.com/users/DarinelCIgarroa/repos"
      );
      const data = await response.json();
      this.projects = data;
      this.loader = false;
    },
  },
  data() {
    return {
      projects: [],
      loader: true,
    };
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  height: auto;
  padding: 20px;
  margin: 20px auto 60px auto;
  box-shadow: 1px 1px 4px black;
}
.cards-item {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>