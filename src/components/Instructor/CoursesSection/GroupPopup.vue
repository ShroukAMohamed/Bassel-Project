<template>
  <div>
    <CancelModal />
    <StudentAttend />
    <div
      class="modal fade"
      id="GroupModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content rounded-4">
          <div class="modal-header d-block text-end">
            <button
              type="button"
              class="btn-close"
              data-bs-dismiss="modal"
              aria-label="Close"
            ></button>
          </div>
          <div class="modal-body d-flex d-md-block justify-content-center">
            <div class="modal-card">
              <div class="d-flex justify-content-center align-items-center">
                <img
                  class="img-fluid"
                  src="../../../assets/laptop_online_working_icon.png"
                  alt=""
                />
                <h3 class="mb-0 ms-3 text-start">Sessions</h3>
              </div>
              <div class="table-responsive dtable-container p-0">
                <table
                  id="myTable"
                  class="table table-striped dt-responsive display nowrap table-bordered mt-5"
                >
                  <thead>
                    <tr>
                      <th>Sessions</th>
                      <th>State</th>
                      <th></th>
                      <th></th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>Session 1</td>
                      <td>Done</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center"
                          disabled
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                    <tr>
                      <td>Session 2</td>
                      <td>Done</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center"
                          disabled
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                    <tr>
                      <td>Session 3</td>
                      <td>Upcoming</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center text-danger"
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                    <tr>
                      <td>Session 4</td>
                      <td>Upcoming</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center text-danger"
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                    <tr>
                      <td>Session 5</td>
                      <td>Upcoming</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center text-danger"
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                    <tr>
                      <td>Session 6</td>
                      <td>Upcoming</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center text-danger"
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                    <tr>
                      <td>Session 7</td>
                      <td>Upcoming</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center text-danger"
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                    <tr>
                      <td>Session 8</td>
                      <td>Upcoming</td>
                      <td
                        data-bs-target="#studentAttendModal"
                        data-bs-toggle="modal"
                        data-bs-dismiss="modal"
                        class="text-center text-success"
                      >
                        Attendance
                      </td>
                      <td>
                        <button
                          data-bs-target="#cancelModal"
                          data-bs-toggle="modal"
                          data-bs-dismiss="modal"
                          class="text-center text-danger"
                        >
                          Cancel
                        </button>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";
import CancelModal from "./CancelModal.vue";
import StudentAttend from "./StudentAttend.vue";
export default {
  name: "GroupPopup",
  components: { CancelModal, StudentAttend },
  mounted() {
    $("#myTable").DataTable({
      columns: [
        { data: "Sessions" },
        { data: "State" },
        { data: "Attendance" },
        { data: "Cancellation" },
      ],
    });
  },
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 1000px;
  .modal-header {
    border-bottom: 1px solid rgb(173, 168, 168);
  }
  .modal-card {
    width: 100%;
    max-width: 800px;
    margin: auto;
    padding-bottom: 20px;
    table {
      width: 100%;
      tr {
        td:nth-child(3),
        td:nth-child(4) {
          cursor: pointer;
        }
        td {
          button {
            border: 0;
            background-color: transparent;
          }
        }
      }
    }
  }
}
</style>
