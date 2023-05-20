<template>
  <div>
    <div
      class="modal fade"
      id="studentAttendModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-5">
          <div class="modal-header">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <form action="">
            <div class="modal-body mb-4">
              <div class="modal-card">
                <h3 class="text-center pb-3 mt-3">
                  <span class="me-3 text-success"
                    ><i class="fa-solid fa-pen-to-square"></i></span
                  >Student Attendance
                </h3>
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
                <AttendCard />
              </div>
            </div>
            <div class="modal-footer d-flex justify-content-center">
              <input
                type="submit"
                value="Sumbit"
                class="validation btn btn-primary rounded-5 pt-2 pb-2 mt-2 mb-2"
              />
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AttendCard from "./Attend_Card.vue";
export default {
  name: "StudentAttend",
  components: { AttendCard },
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 600px;

  .modal-footer {
    input {
      width: 100%;
      max-width: 250px;
    }
  }
}
</style>
