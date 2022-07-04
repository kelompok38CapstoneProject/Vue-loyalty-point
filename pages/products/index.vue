<template>
  <div class="container">
    <b-breadcrumb
      style="background-color: #f4f6f8; margin-left: -15px"
      :items="items"
    ></b-breadcrumb>
    <div class="text-xl">Overview Stock Pulsa</div>
    <div class="my-4">
      <ListGroup />
    </div>

    <div>
      <div class="card rounded-md">
        <div
          class="card-header text-white text-md rounded-md"
          style="background-color: #3252df"
        >
          Product Data Table
        </div>
        <div class="card-body">
          <div class="d-flex justify-content-between">
            <div class="w-25">
              <div class="form-group has-search">
                <span class="fa fa-search form-control-feedback"></span>
                <input
                  type="text"
                  class="form-control"
                  placeholder="Cari data produk"
                  style="background-color: #f4f6f8"
                />
              </div>
            </div>
            <div style="margin-right: 200px">
              <select
                class="form-select"
                aria-label="Default select example"
                style="width: 165px; height: 38px"
              >
                <option selected>All Providers</option>
                <option value="1">Telkomsel</option>
                <option value="2">IM3</option>
                <option value="3">XL</option>
              </select>

              <select
                class="form-select"
                aria-label="Default select example"
                style="width: 165px; height: 38px"
              >
                <option selected>All Stock</option>
                <option value="1">Ready</option>
                <option value="2">Low Stock</option>
                <option value="3">Out of Stock</option>
              </select>
            </div>

            <div>
              <span class="mr-2">
                <b-button @click="clearSelected" variant="outline-danger"
                  ><i class="fas fa-trash-alt"></i
                ></b-button>
              </span>

              <b-button
                id="show-btn"
                @click="$bvModal.show('bv-modal-example')"
                style="background-color: #3252df !important; color: white"
                >Tambah Produk
                <span class="text-sm"><i class="fas fa-plus"></i></span
              ></b-button>
              <!-- Form -->
              <b-modal id="bv-modal-example" hide-footer>
                <template #modal-title> Tambah Products </template>
                <div class="d-block text-center">
                  <b-form-input
                    id="inline-form-input-name"
                    class="mb-2 mr-sm-2 mb-sm-0"
                    placeholder="Nama Product"
                  ></b-form-input>
                  <br />
                  <b-form-select
                    v-model="selected"
                    :options="options"
                    class="mb-3"
                  >
                    <!-- This slot appears above the options from 'options' prop -->
                    <template #first>
                      <b-form-select-option :value="null" disabled
                        >-- Please select an option --</b-form-select-option
                      >
                    </template>

                    <!-- These options will appear after the ones from 'options' prop -->
                    <b-form-select-option value="C"
                      >Option C</b-form-select-option
                    >
                    <b-form-select-option value="D"
                      >Option D</b-form-select-option
                    >
                  </b-form-select>

                  <br />
                  <b-form-input
                    id="inline-form-input-name"
                    class="mb-2 mr-sm-2 mb-sm-0"
                    placeholder="Stocks"
                  ></b-form-input>
                  <br />
                  <b-form-input
                    id="inline-form-input-name"
                    class="mb-2 mr-sm-2 mb-sm-0"
                    placeholder="Point dibutuhkan"
                  ></b-form-input>
                  <br />
                  <b-form-select
                    v-model="selected"
                    :options="options"
                    class="mb-3"
                  >
                    <!-- This slot appears above the options from 'options' prop -->
                    <template #first>
                      <b-form-select-option :value="null" disabled
                        >-- Please select an option --</b-form-select-option
                      >
                    </template>

                    <!-- These options will appear after the ones from 'options' prop -->
                    <b-form-select-option value="C"
                      >Option C</b-form-select-option
                    >
                    <b-form-select-option value="D"
                      >Option D</b-form-select-option
                    >
                  </b-form-select>

                  <br />
                </div>
                <section class="d-flex mt-3 justify-content-end">
                  <b-button
                    class="button-close mr-4"
                    @click="$bvModal.hide('bv-modal-example')"
                    >Close</b-button
                  >
                  <b-button class="button-save" block>Save</b-button>
                </section>
              </b-modal>
              <!-- End Form -->
            </div>
          </div>
          <section>
            <table class="table table-striped">
              <thead>
                <tr>
                  <th scope="col">#</th>
                  <th scope="col">Nama Produk</th>
                  <th scope="col">Stock</th>
                  <th scope="col">Point Dibutuhkan</th>
                  <th scope="col">Updated Date</th>
                  <th scope="col">Status</th>
                  <th scope="col">Action</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="(product, index) in products" :key="index">
                  <td>{{ product.id }}</td>
                  <td>{{ product.name }} {{ product.description }}</td>
                  <td>{{ product.stock }}</td>
                  <td>{{ product.price }}</td>
                  <td>{{ product.UpdatedAt }}</td>
                  <td>
                    <b-button
                      pill
                      style="
                        background-color: #96db69;
                        border-color: #96db69;
                        color: #152c5b;
                      "
                      >Ready</b-button
                    >
                    <b-button
                      pill
                      style="
                        background-color: #ffeb55;
                        border-color: #ffeb55;
                        color: #152c5b;
                      "
                      >Low Stock</b-button
                    >
                    <b-button
                      pill
                      style="
                        background-color: #f67575;
                        border-color: #f67575;
                        color: #152c5b;
                      "
                      >Out of Stock</b-button
                    >
                  </td>
                  <td>
                    <b-dropdown class="mx-1" right>
                      <b-dropdown-item
                        ><i class="fas fa-pencil"></i> Update</b-dropdown-item
                      >
                      <b-dropdown-item
                        ><i class="fas fa-trash"></i> Delete</b-dropdown-item
                      >
                    </b-dropdown>
                  </td>
                </tr>
              </tbody>
            </table>
          </section>

          <section
            class="d-flex justify-content-between align-items-center mt-5"
          >
            <div>
              <h6>Show per page {{ currentPage }}</h6>
            </div>

            <b-pagination
              v-model="currentPage"
              :total-rows="rows"
              :per-page="perPage"
              aria-controls="my-table"
            ></b-pagination>
          </section>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      perPage: 5,
      currentPage: 1,
      products: [],
      modes: ['multi', 'single', 'range'],
      fields: [],
      items: [
        {
          text: 'Dashboard',
          href: '#',
        },
        {
          text: 'Product',
          href: '#',
        },
        {
          text: 'Pulsa',
          active: true,
        },
      ],
      selectMode: 'multi',
      selected: [],
    }
  },
  async fetch() {
    this.products = await fetch('http://13.229.128.27:8080/benefits/').then(
      (res) => res.json()
    )
  },

  computed: {
    rows() {
      return this.items.length
    },
  },
  methods: {
    onRowSelected(items) {
      this.selected = items
    },
    selectAllRows() {
      this.$refs.selectableTable.selectAllRows()
    },
    clearSelected() {
      this.$refs.selectableTable.clearSelected()
    },
  },
}
</script>
<style>
.modal-header {
  color: white;
  background-color: #3252df;
}
.close {
  color: white;
}
</style>