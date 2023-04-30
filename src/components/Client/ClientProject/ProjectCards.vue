<template>
  <div class="mt-4 Parent">
    <div class="d-flex justify-content-between">
      <span>{{ Milestone_title }}</span>
      <span>{{ Status }}</span>
    </div>
    <div class="d-flex justify-content-between">
      <span>{{ ProjDate }}</span>
      <span>see more <i class="fa-solid fa-caret-down"></i></span>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectCards",
  props: ["Milestone_title", "Status", "ProjDate"],
};
</script>

<style lang="scss" scoped>
.Parent {
  background-color: white;
  box-shadow: 0px 3px 6px #00000029;
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
</style>
