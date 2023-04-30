<template>
  <div class="AttendCheck d-flex">
    <span><i class="fa-solid fa-circle-check"></i></span>
    <div class="ms-3">
      <span> Session Title goes here</span>
      <p class="mt-1">12 Mar, Mon <span>12:1 pm</span></p>
    </div>
  </div>
</template>

<script>
export default {
  name: "AttendCheck",
};
</script>

<style lang="scss" scoped>
.AttendCheck {
  > span {
    font-size: 20px;
    color: #5156618f;
  }
  span.active {
    color: #309100;
  }
  div {
    span {
      color: #4a505d;
      font-size: 18px;
    }
    p {
      color: #515661;
      font-size: 18px;
      span {
        color: #010101;
        font-size: 14px;
      }
    }
  }
}
</style>
