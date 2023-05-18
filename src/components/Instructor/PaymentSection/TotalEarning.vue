<template>
  <div>
    <div
      class="modal fade"
      id="TotalModal"
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
                  src="../../../assets/business tools_rich_money bag_icon.png"
                  alt=""
                />
                <h3 class="mb-0 ms-3 text-start">Total Earnings</h3>
              </div>
              <div class="table-responsive dtable-container p-0 mt-4">
                <table
                  id="TotalTable"
                  class="table table-striped dt-responsive display nowrap table-bordered mt-5"
                >
                  <thead>
                    <tr>
                      <th>Groups</th>
                      <th>Earnings</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>Group 1</td>
                      <td>$1000</td>
                    </tr>
                    <tr>
                      <td>Group 2</td>
                      <td>$500</td>
                    </tr>
                    <tr>
                      <td>Group 3</td>
                      <td>$800</td>
                    </tr>
                    <tr>
                      <td>Group 4</td>
                      <td>$600</td>
                    </tr>
                    <tr>
                      <td>Group 5</td>
                      <td>$900</td>
                    </tr>
                    <tr>
                      <td>Group 6</td>
                      <td>$1000</td>
                    </tr>
                    <tr>
                      <td>Group 7</td>
                      <td>$600</td>
                    </tr>
                    <tr>
                      <td>Group 8</td>
                      <td>$500</td>
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
export default {
  name: "TotalEarning",
  mounted() {
    $("#TotalTable").DataTable({
      columns: [{ data: "Groups" }, { data: "Earning" }],
    });
  },
};
</script>

<style lang="scss" scoped>
.modal-dialog {
  max-width: 700px;
  .modal-header {
    border-bottom: 1px solid rgb(173, 168, 168);
  }
  .modal-card {
    width: 100%;
    max-width: 600px;
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
