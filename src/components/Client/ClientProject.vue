<template>
  <div class="Card">
    <div class="p-sm-4 p-3">
      <div class="d-flex justify-content-between">
        <p class="mb-0">
          Project Name - <span>{{ ProjectName }}</span>
        </p>
        <span class="text-center"
          ><i class="fa-solid fa-clock"></i> {{ Status }}</span
        >
      </div>
      <p class="mt-2 mb-2">
        {{ ProjDetails }}
      </p>
      <span
        ><i class="fa-solid fa-calendar-days"></i> Start Date:
        {{ start_date }}</span
      >
      <div class="line mt-3"></div>
      <p class="mt-2 mb-2">Milestones {{ milestones_num }}</p>
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
      <ProjectCard
        :Milestone_title="Milestone_title"
        :Status="Status"
        :ProjDate="ProjDate"
      />
      <button
        class="mt-4 mb-3"
        data-bs-target="#mileModal"
        data-bs-toggle="modal"
        data-bs-dismiss="modal"
      >
        Open More
      </button>
    </div>
  </div>
</template>

<script>
import ProjectDetails from "./ClientProject/ProjectDetails.vue";
import ProjectCard from "./ClientProject/ProjectCards.vue";
export default {
  name: "ClientProject",
  components: { ProjectDetails, ProjectCard },
  data() {
    return {
      ProjectName: "Web Development",
      Status: "Status",
      ProjDetails:
        "Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi in nibh faucibus, iaculis lorem vitae, cursus velit.",
      start_date: "1/1/2023 - 1/1/2024",
      milestones_num: "20",
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
};
</script>

<style lang="scss" scoped>
@import "../global/scss/main.scss";
.Card {
  width: 100%;
  max-width: 460px;
  margin: auto !important;
  padding: 0 !important;
  margin-top: 30px !important;
  background-color: #f6f6f6 !important;
  box-shadow: none;
  .line {
    border-bottom: 1px solid rgb(206, 205, 205);
  }
  > div {
    > div:first-child {
      p {
        font-size: 17px;
        letter-spacing: 0.5px;
        span {
          font-weight: 300;
        }
      }
      > span {
        color: rgb(0, 156, 0);
        font-size: 17px;
      }
    }
    > p:first-of-type {
      color: #646b79;
      font-size: 18px;
      font-weight: 300;
      max-width: 450px;
      letter-spacing: 0.8px;
    }
    > span:first-of-type {
      font-size: 17px;
      font-weight: 500;
      letter-spacing: 0.5px;
    }
    > p:nth-of-type(2) {
      font-size: 18px;
      letter-spacing: 0.5px;
    }

    > div:last-of-type {
      background-color: white;
      padding: 10px 15px;
      > div {
        span:first-of-type {
          color: rgb(88, 87, 87);
        }
      }
      > div:first-child {
        span:first-of-type {
          font-size: 18px;
          letter-spacing: 0.5px;
        }
        span:last-of-type {
          color: #4bc50f;
        }
      }
      > div:last-child {
        span:last-of-type {
          font-size: 14px;
          cursor: pointer;
        }
      }
    }
    > button:last-child {
      border: 0;
      background-color: transparent;
      color: #6864b9;
      text-decoration: underline;
      font-weight: 600;
      letter-spacing: 0.5px;
    }
  }
}
</style>
