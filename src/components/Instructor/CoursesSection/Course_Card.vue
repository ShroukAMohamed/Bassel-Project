<template>
  <div class="parent">
    <h3 class="ms-5">Group 1</h3>
    <div class="ms-5 mt-4">
      <h4 class="pb-4">Front-End</h4>
      <p>
        <span><i class="fa-solid fa-laptop"></i></span> Remaining Sessions :
        <span>10</span>
      </p>
      <p>
        <span><i class="fa-regular fa-clock"></i></span>
        Remaining Hours : <span>90</span>
      </p>
      <p>
        <span><i class="fa-regular fa-calendar"></i></span>
        Start Date : <span>20/9/2023</span>
      </p>
      <p>
        <span><i class="fa-regular fa-calendar-check"></i></span>
        End Date : <span>20/10/2023</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Course_Card",
};
</script>

<style lang="scss" scoped>
.parent {
  h3 {
    font-size: 28px;
  }
  h4 {
    color: #0d6efd;
    font-size: 30px;
  }
  p {
    font-size: 16px;
    margin-bottom: 30px;
    color: rgb(100, 100, 100);
    span:first-child {
      margin-right: 8px;
      color: #147ad6;
      font-size: 18px;
    }
  }
}
</style>
