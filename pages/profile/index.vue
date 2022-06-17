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
            id="show-btn"
            @click="$bvModal.show('bv-modal-example')"
            style="background-color: #3252df !important; color: white"
            >Edit Profile
          </b-button>
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
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Username</label>
                  <input
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Password</label>
                  <input
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
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Role</label>
                  <input
                    type="text"
                    class="form-control"
                    placeholder="First name"
                    aria-label="First name"
                  />
                </div>
                <div class="my-2">
                  <label class="form-label text-base">Phone Number</label>
                  <input
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
      items: [
        {
          text: 'Admin',
          href: '#',
        },
        {
          text: 'Manage',
          href: '#',
        },
        {
          text: 'Library',
          active: true,
        },
      ],
    }
  },
}
</script>

<style>
</style>