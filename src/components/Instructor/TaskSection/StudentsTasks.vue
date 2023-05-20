<template>
  <div class="smallCard d-flex justify-content-center mt-4">
    <img class="img-fluid" src="../../../assets/cheif1.jpg" alt="" />
    <div class="ms-3">
      <p class="mb-0">
        William Smith
        <span class="ms-1 text-success"
          ><i class="fa-solid fa-circle-check"></i
        ></span>
      </p>
      <div>
        <span
          data-bs-target="#SeeTaskModal"
          data-bs-toggle="modal"
          data-bs-dismiss="modal"
          class="me-2"
        >
          See Task
        </span>
        <span
          data-bs-target="#RateTaskModal"
          data-bs-toggle="modal"
          data-bs-dismiss="modal"
        >
          Rate Task
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "StudentsTasks",
};
</script>

<style lang="scss" scoped>
.smallCard {
  background-color: white;
  box-shadow: 0px 3px 12px #00000029;
  width: 100%;
  max-width: 300px;
  margin: auto;
  padding: 15px 0;
  border-radius: 25px;
  img {
    position: relative;
    top: 0;
    left: 0;
    width: 48px;
    object-fit: cover;
    height: 48px;
    border-radius: 50%;
  }
  > div {
    p {
      span {
        font-size: 15px;
      }
    }
    > div {
      span {
        font-size: 14px;
        font-weight: 500;
        cursor: pointer;
      }
      span:nth-child(2) {
        color: #ffa200;
      }
    }
  }
}
</style>
