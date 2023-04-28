<template>
  <div class="Home">
    <HomeComponent />
    <ServicesComponent />
    <div class="container">
      <div class="line"></div>
    </div>
    <CoursesComponent />
    <ChartsComponent />
    <div class="container">
      <div class="line"></div>
    </div>
    <ProjectsComponent />
    <div class="container">
      <div class="line"></div>
    </div>
    <JobsComponent />
    <AboutComponent />
    <ContactComponent />
    <FooterA />
  </div>
</template>

<style lang="scss" scoped>
@import "@/components/global/scss/main.scss";
.line {
  border-bottom: 1px solid black;
  margin: 50px 0;
}
</style>

<script>
import FooterA from "../components/global/Footer.vue";
import HomeComponent from "../components/HomeView/Home";
import ServicesComponent from "../components/HomeView/Services.vue";
import CoursesComponent from "../components/HomeView/Courses.vue";
import ChartsComponent from "../components/HomeView/Charts.vue";
import ProjectsComponent from "../components/HomeView/Projects.vue";
import JobsComponent from "../components/HomeView/Jobs.vue";
import AboutComponent from "../components/HomeView/About.vue";
import ContactComponent from "../components/HomeView/Contact.vue";
export default {
  name: "HomeView",
  components: {
    FooterA,
    HomeComponent,
    ServicesComponent,
    CoursesComponent,
    ChartsComponent,
    ProjectsComponent,
    JobsComponent,
    AboutComponent,
    ContactComponent,
  },
};
</script>
