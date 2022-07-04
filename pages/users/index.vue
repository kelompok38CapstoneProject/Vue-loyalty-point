<template>
  <div class="container">
    <div class="text-xl mb-3">Users Management</div>
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
                  placeholder="Cari data customer"
                  style="background-color: #f4f6f8"
                />
              </div>
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
                >Tambah User
                <span class="text-sm"><i class="fas fa-plus"></i></span
              ></b-button>
              <!-- Form -->
              <b-modal id="bv-modal-example" hide-footer>
                <template #modal-title style="background-color: #3252df">
                  Tambah User
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
                    placeholder="Phone Number"
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
            <table class="table table-striped">
              <thead>
                <tr>
                  <th scope="col">#</th>
                  <th scope="col">Name</th>
                  <th scope="col">Email</th>
                  <th scope="col">Phone Number</th>
                  <th scope="col">Total Point</th>
                  <th scope="col">Created Date</th>
                  <th scope="col">Action</th>
                </tr>
              </thead>
              <tbody>
                <tr class="users" v-for="(user, index) in users" :key="index">
                  <td>{{ user.id }}</td>
                  <td>{{ user.name }}</td>
                  <td>{{ user.email }}</td>
                  <td>{{ user.phone }}</td>
                  <td>{{ user.point }}</td>
                  <td>{{ user.CreatedAt }}</td>
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
import axios from 'axios'
export default {
  data() {
    return {
      perPage: 5,
      currentPage: 1,
      users: [],
    }
  },
  // async fetch() {
  //   this.users = await fetch('http://13.229.128.27:8080/users/').then((res) =>
  //     res.json()
  //   )
  // },
  // Vue axios GET request
  async fetch() {
    try {
      const users = await axios.get('http://13.229.128.27:8080/users/')

      this.users = users.data
    } catch (e) {
      console.log(e)
    }
  },
  // Vue axios POST request
  async storeUser() {
    try {
      const users = await axios.post('http://13.229.128.27:8080/users/', {
        name: this.name,
        email: this.email,
        phone: this.phone,
        point: this.point,
        CreatedAt: this.CreatedAt,
      })

      console.log(users)
    } catch (e) {
      console.log(e)
    }
  },
  // Vue axios PUT request
  async updateUser() {
    try {
      const users = await axios.put(
        'http://13.229.128.27:8080/users/' + this.user.id,
        {
          name: this.user.name,
          email: this.user.email,
        }
      )

      console.log(user.data)
      alert('User updated!')
    } catch (e) {
      console.log(e)
    }
  },
  // Vue axios DELETE request
  async deleteUser(id) {
    let x = window.confirm('You want to delete the user?')

    if (x) {
      const users = await axios.delete('http://13.229.128.27:8080/users/' + id)

      console.log(users)
      alert('User deleted!')
    }
  },
  methods: {},
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