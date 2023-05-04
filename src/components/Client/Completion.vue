<template>
  <div class="Card m-auto">
    <h3>Project Completion</h3>
    <div class="line"></div>
    <div class="d-flex justify-content-between align-items-center pt-3 pb-3">
      <div>
        <p>Project Name</p>
        <p><span>20/50</span> Milestones</p>
        <span>60% completed</span>
      </div>
      <img class="img-fluid" src="../../assets/wavy-line.png" alt="" />
    </div>
    <div class="line"></div>
    <div class="d-flex justify-content-between align-items-center pt-3">
      <div>
        <p>Project Name</p>
        <p><span>20/50</span> Milestones</p>
        <span>60% completed</span>
      </div>
      <img class="img-fluid" src="../../assets/wavy-line2.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "CProjects",
};
</script>

<style lang="scss" scoped>
.Card {
  max-width: 360px;
  padding: 20px 30px;
  h3 {
    font-size: 22px;
    font-family: "Poppins", sans-serif;
  }
  img {
    width: 30%;
    height: 30%;
  }
  .line {
    border-bottom: 1px solid rgb(206, 205, 205);
  }

  div {
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
  div:nth-child(5) {
    span:nth-child(3) {
      color: #4bc50f;
    }
  }
}
</style>
