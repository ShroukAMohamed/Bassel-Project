<template>
  <div>
    <div
      class="d-flex justify-content-between align-items-center pt-3 pb-3"
      data-bs-target="#attendModal"
      data-bs-toggle="modal"
      data-bs-dismiss="modal"
    >
      <div>
        <p>{{ Course_Name }}</p>
        <p>
          <span>{{ Session_Num }}</span> sessions
        </p>
        <span>{{ Completion }} completed</span>
      </div>
      <img class="img-fluid" src="../../assets/wavy-line.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "AttendState",
  props: ["Course_Name", "Session_Num", "Completion"],
};
</script>

<style lang="scss" scoped>
.Card {
  max-width: 400px;
  padding: 20px;
  img {
    width: 30%;
    margin: auto;
    height: 30%;
  }
  div {
    cursor: pointer;
    p:first-of-type {
      font-size: 15px;
      color: #707070;
      margin-bottom: 8px;
    }
    p:last-of-type {
      font-size: 17px;
      margin-bottom: 8px;
      span {
        font-size: 20px;
      }
    }
    span:nth-child(3) {
      color: #ff2366;
      font-weight: 300;
      font-size: 13px;
    }
  }
}
</style>
