<template>
  <div>
    <section class="available-jobs pt-4 pb-4">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-12 text-center">
            <h2 class="fw-bold">Our Available Jobs</h2>
          </div>
          <div class="col-xl-5 col-md-6 col-12">
            <AvJobs />
          </div>
          <div class="col-xl-5 col-md-6 col-12 pt-5 pt-md-0">
            <AvJobs />
          </div>
          <div class="col-xl-5 col-md-6 col-12 pt-5">
            <AvJobs />
          </div>
          <div class="col-xl-5 col-md-6 col-12 pt-5">
            <AvJobs />
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
