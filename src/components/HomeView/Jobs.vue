<template>
  <div>
    <section id="Jobs" class="available-jobs block pt-4 pb-4">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-12 text-center">
            <h2 class="fw-bold">Our Available Jobs</h2>
          </div>
          <div
            data-aos="zoom-in-left"
            data-aos-duration="1000"
            class="col-xl-5 col-md-6 col-12"
          >
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
          <div
            data-aos="zoom-in-left"
            data-aos-duration="1000"
            class="col-xl-5 col-md-6 col-12 pt-5 pt-md-0"
          >
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
          <div
            data-aos="zoom-in-left"
            data-aos-duration="1000"
            class="col-xl-5 col-md-6 col-12 pt-5"
          >
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
          <div
            data-aos="zoom-in-left"
            data-aos-duration="1000"
            class="col-xl-5 col-md-6 col-12 pt-5"
          >
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
        </div>
        <div class="HideSection">
          <div class="row justify-content-center">
            <div class="col-xl-5 col-md-6 col-12 gy-5">
              <AvJobs
                :name="Job_title"
                :requirements="required"
                :details="Job_details"
              />
            </div>
            <div class="col-xl-5 col-md-6 col-12 gy-5">
              <AvJobs
                :name="Job_title"
                :requirements="required"
                :details="Job_details"
              />
            </div>
          </div>
          <div class="row justify-content-center">
            <div class="col-xl-5 col-md-6 col-12 gy-5">
              <AvJobs
                :name="Job_title"
                :requirements="required"
                :details="Job_details"
              />
            </div>
            <div class="col-xl-5 col-md-6 col-12 gy-5">
              <AvJobs
                :name="Job_title"
                :requirements="required"
                :details="Job_details"
              />
            </div>
          </div>
        </div>
        <div class="text-center">
          <button
            @click="showFunction('.HideSection', '.ShowJobs', '.HideJobs')"
            class="ShowJobs mt-5"
          >
            See More
          </button>
        </div>
        <div class="text-center">
          <button
            @click="hideFunction('.HideSection', '.ShowJobs', '.HideJobs')"
            class="HideJobs mt-5"
          >
            See Less
          </button>
        </div>
      </div>
    </section>
    <jobsPopup />
  </div>
</template>

<script>
import jobsPopup from "./AvailableJobs/jobsPopup.vue";
import AvJobs from "./AvailableJobs/AvJobs.vue";
import show_btn from "../../../mixin/show_btn.vue";
export default {
  name: "JobsComponents",
  data() {
    return {
      Job_title: "Job Title",
      required: "3 years experience -salary: 5000 egp",
      Job_details:
        "Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi in nibh faucibus, iaculis lorem vitae, cursus velit.",
    };
  },
  components: { jobsPopup, AvJobs },
  mixins: [show_btn],
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.available-jobs {
  h2 {
    font-size: 40px;
    letter-spacing: 1px;
    padding-bottom: 50px;
    font-family: "Poppins", sans-serif;
    @include breakpoints(mobile) {
      font-size: 32px;
    }
  }

  div {
    button:first-child {
      border: 0;
      background-color: transparent;
      padding: 10px 60px;
      color: whitesmoke;
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 1px;
      background: transparent linear-gradient(180deg, #6864b9 0%, #6864b9 100%)
        0% 0% no-repeat padding-box;
      box-shadow: 0px 3px 6px #292341;
      border-radius: 18px;
      opacity: 1;
      transition: all 0.3s;
      &:hover {
        transform: translateY(-6px);
      }
    }
  }
  .HideSection {
    display: none;
  }
  .HideJobs {
    display: none;
  }
}
</style>
