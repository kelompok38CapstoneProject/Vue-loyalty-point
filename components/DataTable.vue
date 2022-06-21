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
            <b-button
              id="show-btn"
              @click="$bvModal.show('bv-modal-example')"
              style="background-color: #3252df !important; color: white"
              >Tambah Produk
              <span class="text-sm"><i class="fas fa-plus"></i></span
            ></b-button>

            <b-modal id="bv-modal-example" hide-footer>
              <template #modal-title style="background-color: #3252df">
                Tambah Customer
              </template>
              <div class="d-block text-center">
                <b-form-input
                  id="inline-form-input-name"
                  class="mb-2 mr-sm-2 mb-sm-0"
                  placeholder="Nama Lengkap"
                ></b-form-input>
                <br />
                <b-form-input
                  id="inline-form-input-name"
                  class="mb-2 mr-sm-2 mb-sm-0"
                  placeholder="Email"
                ></b-form-input>
                <br />
                <b-form-input
                  id="inline-form-input-name"
                  class="mb-2 mr-sm-2 mb-sm-0"
                  placeholder="Nomor telepon"
                ></b-form-input>
                <br />
                <b-form-input
                  id="inline-form-input-name"
                  class="mb-2 mr-sm-2 mb-sm-0"
                  placeholder="Password"
                ></b-form-input>
                <br />
                <b-form-input
                  id="inline-form-input-name"
                  class="mb-2 mr-sm-2 mb-sm-0"
                  placeholder="Point"
                ></b-form-input>
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
          <div class="mt-3">
            <b-table
              responsive
              striped
              hover
              id="my-table"
              :per-page="perPage"
              :current-page="currentPage"
              :items="items"
              thead-class="primaryColor"
            ></b-table>
          </div>
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
      items: [
        {
          No: 1,
          Username: 'Dickerson',
          Email: 'Macdonald',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 2,
          Username: 'Larsen',
          Email: 'Shaw',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 3,
          Username: 'Geneva',
          Email: 'Wilson',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 4,
          Username: 'Jami',
          Email: 'Carney',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 5,
          Username: 'Jami',
          Email: 'Carney',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 6,
          Username: 'Jami',
          Email: 'Carney',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 7,
          Username: 'Jami',
          Email: 'Carney',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 8,
          Username: 'Jami',
          Email: 'Carney',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 9,
          Username: 'Jami',
          Email: 'Carney',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
        {
          No: 10,
          Username: 'Jami',
          Email: 'Carney',
          PhoneNumber: '12321',
          TotalPoint: '12321',
          CreatedDate: '10-12-2022',
        },
      ],
    }
  },
  computed: {
    rows() {
      return this.items.length
    },
  },
}
</script>

<style>
.primaryColor,
.table thead th,
thead,
th {
  background-color: #3252df !important;
  color: white;
}
.rounded-md {
  border-radius: 10px;
}

.has-search .form-control {
  padding-left: 2.375rem;
}

.has-search .form-control-feedback {
  position: absolute;
  z-index: 2;
  display: block;
  width: 2.375rem;
  height: 2.375rem;
  line-height: 2.375rem;
  text-align: center;
  pointer-events: none;
  color: #aaa;
}

.button-save {
  background-color: #3252df;
  width: 100px;
  height: 40px;
}

.button-save:hover {
  background-color: #163ef1;
  border: 2px solid #3252df;
}

.button-close {
  border: 2px solid #3252df;
  background-color: #fff;
  width: 100px;
  height: 40px;
  color: #163ef1;
}

.button-close:hover {
  border: 2px solid #3252df;
  background-color: #3252df;
  color: #fff;
}
</style>