<template>
  <div class="container" style="max-width: 1000px">
    <div class="row mt-3">
      <nav aria-label="breadcrumb">
        <ol class="breadcrumb">
          <li class="breadcrumb-item">
            <router-link class="text-dark" to="/">Dashboard</router-link>
          </li>
          <li class="breadcrumb-item active text-dark" aria-current="page">
            Products Management
          </li>
          <li
            class="breadcrumb-item active text-dark"
            aria-current="page"
            style="color: #3252df"
          >
            Pulsa
          </li>
        </ol>
      </nav>
    </div>
    <h1>Overview Stock Pulsa</h1>
    <table class="table table-bordered mt-5">
      <thead style="background-color: #3252df !important; color: white">
        <tr>
          <th scope="col" class="text-left">Produk Data Table</th>
        </tr>
      </thead>

      <b-button
        style="
          background-color: #3252df !important;
          color: white;
          margin-top: 30px;
        "
        >Tambah Produk</b-button
      >
      <table class="table table-bordered mt-5">
        <thead style="background-color: #3252df !important; color: white">
          <tr>
            <th scope="col" class="text-center">No</th>
            <th scope="col" class="text-center">Nama Produk</th>
            <th scope="col" class="text-center">Stock</th>
            <th scope="col" class="text-center">Phone Number</th>
            <th scope="col" class="text-center">Updated Date</th>
            <th scope="col" class="text-center">Status</th>
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
            <td class="text-center">Telkomsel Pulsa 5000</td>
            <td class="text-center">100</td>
            <td class="text-center">20.000</td>
            <td class="text-center">10-12-2022</td>
            <td class="text-center">
              <b-button pill variant="success">Ready</b-button>
            </td>
            <td class="text-center">
              <button class="bi bi-info-circle">Action</button>
            </td>
          </tr>
          <tr style="background-color: #f2f2f2 !important">
            <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
            <td class="text-center">Telkomsel Pulsa 5000</td>
            <td class="text-center">100</td>
            <td class="text-center">20.000</td>
            <td class="text-center">10-12-2022</td>
            <td class="text-center">
              <b-button pill variant="success">Ready</b-button>
            </td>
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
            <td class="text-center">Telkomsel Pulsa 5000</td>
            <td class="text-center">100</td>
            <td class="text-center">20.000</td>
            <td class="text-center">10-12-2022</td>
            <td class="text-center">
              <b-button pill variant="success">Ready</b-button>
            </td>
            <td class="text-center">
              <button class="bi bi-info-circle">Action</button>
            </td>
          </tr>
          <tr style="background-color: #f2f2f2 !important">
            <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
            <td class="text-center">Telkomsel Pulsa 5000</td>
            <td class="text-center">100</td>
            <td class="text-center">20.000</td>
            <td class="text-center">10-12-2022</td>
            <td class="text-center">
              <b-button pill variant="success">Ready</b-button>
            </td>
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
            <td class="text-center">Telkomsel Pulsa 5000</td>
            <td class="text-center">100</td>
            <td class="text-center">20.000</td>
            <td class="text-center">10-12-2022</td>
            <td class="text-center">
              <b-button pill variant="warning">Low Stock</b-button>
            </td>
            <td class="text-center">
              <button class="bi bi-info-circle">Action</button>
            </td>
          </tr>
          <tr style="background-color: #f2f2f2 !important">
            <td class="text-center">
              <label class="checkbox-wrap checkbox-primary">
                <input type="checkbox" checked="" />
                <span class="checkmark"></span>
              </label>
            </td>
            <td class="text-center">Telkomsel Pulsa 5000</td>
            <td class="text-center">100</td>
            <td class="text-center">20.000</td>
            <td class="text-center">10-12-2022</td>
            <td class="text-center">
              <b-button pill variant="danger">Out of stock</b-button>
            </td>
            <td class="text-center">
              <button class="bi bi-info-circle">Action</button>
            </td>
          </tr>
        </tbody>
      </table>
    </table>
    <div class="d-flex mt-5"></div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      // items: [{}, {}],
    }
  },
}
</script>