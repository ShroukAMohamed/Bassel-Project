<template>
  <div>
    <section class="our-projects">
      <div class="project-img">
        <div class="container">
          <div class="row justify-content-center pb-5 pt-3">
            <div class="col-12 text-center mb-5">
              <h2 class="fw-bold">OUR PROJECTS</h2>
            </div>
            <div class="col-xl-5 col-md-6 col-12 gy-4 gy-lg-0">
              <div class="Project">
                <img
                  class="img-fluid pb-5"
                  src="../../assets/projects.png"
                  alt=""
                />
                <ProjSection
                  :name="project_name"
                  :Track="track_name"
                  :date="project_date"
                  :review="Review"
                  :person="Person"
                  :job="Job"
                />
              </div>
            </div>
            <div class="col-xl-5 col-md-6 col-12 gy-5 gy-md-0">
              <div class="Project">
                <ProjSection
                  :name="project_name"
                  :Track="track_name"
                  :date="project_date"
                  :review="Review"
                  :person="Person"
                  :job="Job"
                />
              </div>
              <div class="Project mt-5">
                <ProjSection
                  :name="project_name"
                  :Track="track_name"
                  :date="project_date"
                  :review="Review"
                  :person="Person"
                  :job="Job"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import ProjSection from "./Projects/Project.vue";
export default {
  name: "ProjectsComponent",
  data() {
    return {
      project_name: "Project Name",
      track_name: "Web Development",
      project_date: "12 Mar 2020",
      Review:
        "Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi in nibh faucibus, iaculis lorem vitae, cursus velit.",
      Person: "Walter Barrett",
      Job: "CEO & Founder",
    };
  },
  components: { ProjSection },
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.our-projects {
  .project-img {
    background-image: url("../../assets/Group281.svg");
    width: 100%;

    background-repeat: no-repeat;
    background-size: cover;
    h2 {
      font-size: 45px;
      letter-spacing: 1px;
      @include breakpoints(mobile) {
        font-size: 35px;
      }
    }

    .Project {
      width: 100%;
      max-width: 500px;
      padding: 2%;
      margin: auto;
      border: 1px solid black;
    }
  }
}
</style>
