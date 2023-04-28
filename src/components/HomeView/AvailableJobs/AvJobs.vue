<template>
  <div class="Job ps-3">
    <div class="d-flex justify-content-between pb-1">
      <span class="fw-bold"
        ><img class="pe-2" src="../../../assets/MaskGroup47.svg" alt="" /> Job
        Title</span
      >
      <button
        data-bs-target="#jobsModal"
        data-bs-toggle="modal"
        data-bs-dismiss="modal"
      >
        Enroll Now
      </button>
    </div>
    <div class="line"></div>
    <span class="d-block pt-1 pb-2">3 years experience -salary: 5000 egp</span>
    <div class="line"></div>
    <p>
      Mauris imperdiet orci dapibus, commodo libero nec, interdum tortor. Morbi
      in nibh faucibus, iaculis lorem vitae, cursus velit.
    </p>
  </div>
</template>

<script>
export default {
  name: "AvJobs",
};
</script>

<style lang="scss" scoped>
.Job {
  width: 100%;
  max-width: 500px;
  padding: 20px 0;
  margin: auto;
  border: 1px solid black;
  p {
    width: 100%;
    max-width: 400px;
    color: #686f7c;
    font-size: 16px;
    letter-spacing: 0.8px;
    padding: 10px 0;
  }
  span {
    color: #292341;
  }
  button {
    margin: 8px;
    padding: 0 15px;
    font-size: 15px;
    border-radius: 25px;
    border: 0;
    background-color: #6864b9;
    box-shadow: 0px 3px 6px #6864b969;
    color: white;
  }
  .line {
    border-bottom: 1px solid #acacada6;
  }
}
</style>
