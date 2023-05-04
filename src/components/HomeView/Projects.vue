<template>
  <div>
    <section id="Projects" class="our-projects block">
      <div class="project-img">
        <div class="container">
          <div class="row justify-content-center pt-3">
            <div class="col-12 text-center mb-5">
              <h2 class="fw-bold">OUR PROJECTS</h2>
            </div>
            <div
              data-aos="fade-in"
              data-aos-duration="1000"
              data-aos-delay="100"
              class="col-xl-5 col-md-6 col-12 gy-4 gy-lg-0"
            >
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
              <div
                data-aos="fade-in"
                data-aos-duration="1000"
                data-aos-delay="200"
                class="Project"
              >
                <ProjSection
                  :name="project_name"
                  :Track="track_name"
                  :date="project_date"
                  :review="Review"
                  :person="Person"
                  :job="Job"
                />
              </div>
              <div
                data-aos="fade-in"
                data-aos-duration="1000"
                data-aos-delay="100"
                class="Project mt-5"
              >
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
          <div class="HideProjects">
            <div class="row justify-content-center">
              <div class="col-xl-5 col-md-6 col-12 gy-5">
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
              </div>
              <div class="col-xl-5 col-md-6 col-12 gy-5">
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
              </div>
            </div>
            <div class="row justify-content-center">
              <div class="col-xl-5 col-md-6 col-12 gy-5">
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
              </div>
              <div class="col-xl-5 col-md-6 col-12 gy-5">
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
              </div>
            </div>
          </div>
          <div class="text-center">
            <button
              @click="showFunction('.HideProjects', '.ShowProj', '.HideProj')"
              class="ShowProj mt-5"
            >
              See More
            </button>
          </div>
          <div class="text-center">
            <button
              @click="hideFunction('.HideProjects', '.ShowProj', '.HideProj')"
              class="HideProj mt-5"
            >
              See Less
            </button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import ProjSection from "./Projects/Project.vue";
import show_btn from "../../../mixin/show_btn.vue";
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
  mixins: [show_btn],
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.our-projects {
  .project-img {
    background-image: url("../../assets/Group281.svg");
    width: 100%;
    h2 {
      font-size: 45px;
      letter-spacing: 1px;
      font-family: "Poppins", sans-serif;
      font-weight: bold;
      @include breakpoints(mobile) {
        font-size: 35px;
      }
    }
    .HideProjects {
      display: none;
    }

    .Project {
      width: 100%;
      max-width: 500px;
      padding: 2%;
      margin: auto;
      border: 1px solid black;
    }

    div {
      button:first-child {
        border: 0;
        background-color: transparent;
        padding: 10px 60px;
        color: whitesmoke;
        font-size: 14px;
        letter-spacing: 1px;
        background: transparent
          linear-gradient(180deg, #2596be 0%, #2503f3 100%) 0% 0% no-repeat
          padding-box;
        box-shadow: 0px 3px 6px #292341;
        border-radius: 18px;
        opacity: 1;
        transition: all 0.3s;
        &:hover {
          transform: translateY(-6px);
        }
      }
    }
    .HideProj {
      display: none;
    }
  }
}
</style>
