<template>
  <div class="container" style="max-width: 1000px">
    <h2 class="text mt-5">Users Management</h2>
    <b-button style="background-color: #3252df !important; color: white"
      >Tambah User</b-button
    >
    <table class="table table-bordered mt-5">
      <thead style="background-color: #3252df !important; color: white">
        <tr>
          <th scope="col" class="text-center">No</th>
          <th scope="col" class="text-center">Username</th>
          <th scope="col" class="text-center">Email</th>
          <th scope="col" class="text-center">Phone Number</th>
          <th scope="col" class="text-center">Total Point</th>
          <th scope="col" class="text-center">Created Date</th>
          <th scope="col" class="text-center">Action</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
          <td class="text-center">Andi</td>
          <td class="text-center">andi@gmail.com</td>
          <td class="text-center">081291273233</td>
          <td class="text-center">10.000</td>
          <td class="text-center">10-12-2022</td>
          <td class="text-center">
            <button class="bi bi-info-circle">Action</button>
          </td>
        </tr>
        <tr style="background-color: #f2f2f2 !important;">
          <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
          <td class="text-center">Ana</td>
          <td class="text-center">ana@gmail.com</td>
          <td class="text-center">081291273233</td>
          <td class="text-center">10.000</td>
          <td class="text-center">10-12-2022</td>
          <td class="text-center">
            <button class="bi bi-info-circle">Action</button>
          </td>
        </tr>
        <tr>
          <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
          <td class="text-center">Hairul</td>
          <td class="text-center">hairul@gmail.com</td>
          <td class="text-center">081291273233</td>
          <td class="text-center">10.000</td>
          <td class="text-center">10-12-2022</td>
          <td class="text-center">
            <button class="bi bi-info-circle">Action</button>
          </td>
        </tr>
        <tr style="background-color: #f2f2f2 !important;">
          <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
          <td class="text-center">james</td>
          <td class="text-center">james@gmail.com</td>
          <td class="text-center">081291273233</td>
          <td class="text-center">10.000</td>
          <td class="text-center">10-12-2022</td>
          <td class="text-center">
            <button class="bi bi-info-circle">Action</button>
          </td>
        </tr>
        <tr>
          <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
          <td class="text-center">Jono</td>
          <td class="text-center">jono@gmail.com</td>
          <td class="text-center">081291273233</td>
          <td class="text-center">10.000</td>
          <td class="text-center">10-12-2022</td>
          <td class="text-center">
            <button class="bi bi-info-circle">Action</button>
          </td>
        </tr>
        <tr style="background-color: #f2f2f2 !important;">
          <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
          <td class="text-center">Hendi</td>
          <td class="text-center">hendi@gmail.com</td>
          <td class="text-center">081291273233</td>
          <td class="text-center">10.000</td>
          <td class="text-center">10-12-2022</td>
          <td class="text-center">
            <button class="bi bi-info-circle">Action</button>
          </td>
        </tr>
      </tbody>
    </table>

    <div class="d-flex mt-5"></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [{}, {}],
    }
  },
}
</script>