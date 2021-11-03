<template>
  <section id="skills" class="light-section">
    <div class="container-fluid">
      <h1 class="section-header">{{ heading }}</h1>
      <img  contain height="170px" width="500px" src="../../assets/images/portfolio/nomics.png"> <br>
      <img  contain height="100px" width="400px" src="../../assets/images/portfolio/coingecko.png"> <br> <br>
      <img  contain height="70px" width="400px" src="../../assets/images/portfolio/cmc.png">



    </div>
    <!-- end of main container  -->
    <Arrow />
  </section>
</template>

<script>
import data from "../../data/data.json";
import Arrow from "../components/Arrow.vue";

export default {
  name: "Skills",
  props: {},
  components: {
    Arrow,
  },
  data() {
    return {
      skills: data.skills.categories,
      heading: data.main.headings.skills,
      currentCategory: data.skills.defaultCategory,
    };
  },
  computed: {
    filteredSkills() {
      var skills = data.skills.categories;
      var category = this.currentCategory;
      var filtered = skills.filter(function(x) {
        if (x.category === category) {
          return x;
        }
      });

      console.log(filtered);

      return filtered;
    },
  },
  methods: {
    setCategory(event) {
      this.currentCategory = event.target.dataset.category;
    },
  },
};
</script>

<style lang="scss"></style>
