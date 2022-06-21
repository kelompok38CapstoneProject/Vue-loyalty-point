<template>
  <div>
    <div class="card rounded-md">
      <div
        class="card-header text-white text-md rounded-md"
        style="background-color: #3252df"
      >
        User Data Table
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

          <div>
            <span class="mr-2">
              <b-button variant="outline-danger"
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

            <b-modal id="bv-modal-example" hide-footer>
              <template #modal-title style="background-color: #3252df">
                Tambah User
              </template>
              <div class="d-block text-center">
                <b-form-input
                  id="inline-form-input-name"
                  class="mb-2 mr-sm-2 mb-sm-0"
                  placeholder="Nama Products"
                ></b-form-input>
                <br />
                <b-form-select
                  v-model="selected"
                  :options="options1"
                  class="mb-3"
                  placeholder="Provider"
                >
                  <!-- This slot appears above the options from 'options' prop -->
                  <template #first>
                    <b-form-select-option :value="null" disabled
                      >Provider</b-form-select-option
                    >
                  </template>
                </b-form-select>
                <br />
                <b-form-input
                  id="inline-form-input-name"
                  class="mb-2 mr-sm-2 mb-sm-0"
                  placeholder="Stock"
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
                  :options="options2"
                  class="mb-3"
                  placeholder="Provider"
                >
                  <!-- This slot appears above the options from 'options' prop -->
                  <template #first>
                    <b-form-select-option :value="null" disabled
                      >Status Product</b-form-select-option
                    >
                  </template>
                </b-form-select>
                <br />
              </div>
              <section class="d-flex mt-3">
                <b-button class="button-save mr-4" block>Save</b-button>
                <b-button
                  class="button-close"
                  @click="$bvModal.hide('bv-modal-example')"
                  >Close</b-button
                >
              </section>
            </b-modal>
            <!-- End Form -->
          </div>
        </div>
        <section>
          <b-table
            striped
            hover
            :per-page="perPage"
            :current-page="currentPage"
            :items="items"
            :fields="fields"
            :select-mode="selectMode"
            responsive="sm"
            ref="selectableTable"
            selectable
            @row-selected="onRowSelected"
          >
            <!-- Example scoped slot for select state illustrative purposes -->
            <template #cell(selected)="{ rowSelected }">
              <template v-if="rowSelected">
                <span aria-hidden="true">&check;</span>
                <span class="sr-only">Selected</span>
              </template>
              <template v-else>
                <span aria-hidden="true">&nbsp;</span>
                <span class="sr-only">Not selected</span>
              </template>
            </template>
          </b-table>
          <p>
            <b-button size="sm" @click="selectAllRows">Select all</b-button>
            <b-button size="sm" @click="clearSelected">Clear selected</b-button>
          </p>
        </section>

        <section class="d-flex justify-content-between align-items-center mt-5">
          <div>
            <h6>Page {{ currentPage }}</h6>
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
</template>

<script>
export default {
  data() {
    return {
      perPage: 5,
      currentPage: 1,
      modes: ['multi', 'single', 'range'],
      fields: [
        'selected',
        'Username',
        'Email',
        'PhoneNumber',
        'TotalPoint',
        'CreatedDate',
        'Action',
      ],
      items: [
        {
          No: 1,
          Username: 'Alvaro',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
        {
          No: 2,
          Username: 'Alvaro',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
        {
          No: 3,
          Username: 'Alvaro3',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
        {
          No: 4,
          Username: 'Alvaro4',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
        {
          No: 5,
          Username: 'Alvaro5',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
        {
          No: 6,
          Username: 'Alvaro6',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
        {
          No: 7,
          Username: 'Alvaro7',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
        {
          No: 8,
          Username: 'Alvaro8',
          Email: 'andrewalvaroh@gmail.com',
          PhoneNumber: '098821312',
          TotalPoint: '123',
          CreatedDate: '10-12-2022',
        },
      ],
      selectMode: 'multi',
      selected: [],
    }
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