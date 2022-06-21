<template>
  <div>
    <b-breadcrumb
      style="background-color: #f4f6f8"
      :items="items"
    ></b-breadcrumb>

    <b-card style="height: 100vh">
      <div
        class="
          d-flex
          align-items-center
          justify-content-between
          border-bottom
          pb-3
        "
      >
        <div class="text-md">My Profile</div>
        <div>
          <b-button
            @click="isEditing = !isEditing"
            v-if="!isEditing"
            id="show-btn"
            style="background-color: #3252df !important; color: white"
            >Edit Profile
          </b-button>
          <b-button
            class="btn btn-sm btn-success me-1"
            @click="save"
            v-else-if="isEditing"
          >
            Save
          </b-button>
          <b-button
            class="btn btn-sm btn-danger"
            v-if="isEditing"
            @click="isEditing = false"
            >Cancel</b-button
          >
        </div>
      </div>

      <section class="mt-3">
        <div class="row">
          <div class="col-3">
            <img
              src="/assets/img/profilee.png"
              class="img-thumbnail"
              alt="admin_profile"
            />
          </div>

          <div class="col-7">
            <div class="row g-3">
              <div class="col">
                <div class="my-2">
                  <label class="form-label text-base">Nama</label>
                  <input
                    ref="first_name"
                    :disabled="!isEditing"
                    :class="{ view: !isEditing }"
                    :value="user.firstName"
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Username</label>
                  <input
                    ref="username"
                    :value="user.username"
                    :disabled="!isEditing"
                    :class="{ view: !isEditing }"
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Password</label>
                  <input
                    ref="password"
                    :value="user.password"
                    :disabled="!isEditing"
                    :class="{ view: !isEditing }"
                    type="password"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
              </div>
              <div class="col">
                <div class="my-2">
                  <label class="form-label text-base">Email</label>
                  <input
                    ref="email"
                    :value="user.email"
                    :disabled="!isEditing"
                    :class="{ view: !isEditing }"
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Role</label>
                  <input
                    ref="role"
                    :value="user.role"
                    :disabled="!isEditing"
                    :class="{ view: !isEditing }"
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Phone Number</label>
                  <input
                    ref="phoneNumber"
                    :value="user.phoneNumber"
                    :disabled="!isEditing"
                    :class="{ view: !isEditing }"
                    type="number"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isEditing: false,
      user: {
        firstName: 'John Doe',
        username: 'johndoe121',
        email: 'demo@gmail.com',
        password: 'password',
        role: 'admin',
        phoneNumber: '087512312',
      },
    }
  },
  methods: {
    save() {
      this.user.firstName = this.$refs['first_name'].value
      this.user.username = this.$refs['username'].value
      this.user.email = this.$refs['email'].value
      this.user.password = this.$refs['password'].value
      this.isEditing = !this.isEditing
    },
  },
}
</script>

<style>
</style>