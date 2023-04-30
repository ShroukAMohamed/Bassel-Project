<template>
  <div>
    <div
      class="modal fade"
      id="mileModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header d-block text-end">
            <div class="ps-3 pe-3">
              <div class="w-100">
                <button
                  type="button"
                  class="btn-close"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                ></button>
              </div>
              <div class="d-flex justify-content-center align-items-center">
                <img
                  class="img-fluid"
                  src="../../assets/MaskGroup47.svg"
                  alt=""
                />
                <h3 class="mb-0 ms-3 text-start">Project Name - Milestones</h3>
              </div>
            </div>
          </div>
          <div class="modal-body d-flex d-md-block justify-content-center">
            <div
              class="modal-card d-flex flex-column-reverse flex-md-row justify-content-around mt-3 mb-5"
            >
              <div class="part-1">
                <ProjectCard
                  :Milestone_title="Milestone_title"
                  :Status="Status"
                  :ProjDate="ProjDate"
                />
                <ProjectCard
                  :Milestone_title="Milestone_title"
                  :Status="Status"
                  :ProjDate="ProjDate"
                />
                <ProjectCard
                  :Milestone_title="Milestone_title"
                  :Status="Status"
                  :ProjDate="ProjDate"
                />
                <ProjectCard
                  :Milestone_title="Milestone_title"
                  :Status="Status"
                  :ProjDate="ProjDate"
                />
                <ProjectCard
                  :Milestone_title="Milestone_title"
                  :Status="Status"
                  :ProjDate="ProjDate"
                />
                <ProjectCard
                  :Milestone_title="Milestone_title"
                  :Status="Status"
                  :ProjDate="ProjDate"
                />
              </div>
              <div class="Line d-none d-md-block"></div>
              <div class="part2">
                <div class="d-flex justify-content-center">
                  <img
                    class="img-fluid"
                    src="../../assets/MaskGroup53-svg.svg"
                    alt=""
                  />
                </div>
                <ProjectDetails
                  :Milestone_title="Milestone_title"
                  :Status="Status"
                  :ProjDate="ProjDate"
                  :ProjSalary="ProjSalary"
                  :Details="Details"
                  :Comment="Comment"
                  :Reply="Reply"
                  :comment_date="Comment_Date"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProjectDetails from "./ClientProject/ProjectDetails.vue";
import ProjectCard from "./ClientProject/ProjectCards.vue";
export default {
  name: "MilePopup",
  data() {
    return {
      Status: "Status",
      Milestone_title: "Milestone Title",
      ProjDate: "12 Jan -12 Mar",
      ProjSalary: "Due : 1000 EGP",
      Details:
        "Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi in nibh faucibus, iaculis lorem vitae, cursus velit. Etiam non",
      Comment:
        "Aliquam in bibendum mauris. Sed vitae erat vel velit blandit pharetra vitae nec ante. Cras at est",
      Reply:
        "Aliquam in bibendum mauris. Sed vitae erat vel velit blandit pharetra vitae nec ante. Cras at est",
      Comment_Date: "12 Mar",
    };
  },
  components: { ProjectDetails, ProjectCard },
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.modal-dialog {
  max-width: 1200px;
  .modal-header {
    border-bottom: 1px solid rgb(173, 168, 168);
  }
  .modal-card {
    .part-1 {
      width: 100%;
      max-width: 450px;
    }
    .Line {
      position: relative;
      margin-top: 20px;
      &::before {
        content: "";
        position: absolute;
        width: 1px;
        height: 780px;
        background-color: rgb(187, 183, 183);
      }
    }

    .part2 {
      .Card-inside {
        background-color: #dbddf738;
        box-shadow: 0px 3px 6px #00000029;
        width: 100%;
        max-width: 450px;
        padding: 10px 20px;
        @include insideCard;
      }
    }
  }
}
</style>
