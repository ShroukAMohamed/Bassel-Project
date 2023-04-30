<template>
  <div>
    <section class="available-jobs pt-4 pb-4">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-12 text-center">
            <h2 class="fw-bold">Our Available Jobs</h2>
          </div>
          <div class="col-xl-5 col-md-6 col-12">
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
          <div class="col-xl-5 col-md-6 col-12 pt-5 pt-md-0">
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
          <div class="col-xl-5 col-md-6 col-12 pt-5">
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
          <div class="col-xl-5 col-md-6 col-12 pt-5">
            <AvJobs
              :name="Job_title"
              :requirements="required"
              :details="Job_details"
            />
          </div>
        </div>
      </div>
    </section>
    <jobsPopup />
  </div>
</template>

<script>
import jobsPopup from "./AvailableJobs/jobsPopup.vue";
import AvJobs from "./AvailableJobs/AvJobs.vue";
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
};
</script>

<style lang="scss" scoped>
@import "../../components/global/scss/main.scss";
.available-jobs {
  h2 {
    font-size: 40px;
    letter-spacing: 1px;
    padding-bottom: 50px;
    @include breakpoints(mobile) {
      font-size: 32px;
    }
  }
}
</style>
