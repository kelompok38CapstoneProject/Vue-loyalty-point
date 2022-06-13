<template>
  <div>
    <header>
      <!-- Sidebar -->
      <nav
        id="sidebarMenu"
        class="collapse d-lg-block sidebar collapse"
        style="background-color: #3252df"
      >
        <div class="d-flex justify-content-center">
          <nuxt-link class="navbar-brand" to="/">
            <img
              src="/assets/img/logo.png"
              height="25"
              alt="MDB Logo"
              loading="lazy"
            />
          </nuxt-link>
        </div>

        <div class="position-sticky">
          <div class="px-3">
            <div
              class="mt-5 py-1 rounded-sm"
              style="background-color: #546fe4; color: #fff"
            >
              <div>
                <div class="d-flex align-items-center">
                  <div class="h2 px-2">
                    <i class="fas fa-user-circle"></i>
                  </div>
                  <div>
                    <span class="text-base">Andi</span> <br />
                    <span class="text-sm">View My Profile</span>
                  </div>
                </div>
              </div>
            </div>
            <div class="mt-5 text-white">
              <span class="text-base"> Main Menu</span>

              <div class="py-2 my-3 rounded-sm sidelink">
                <div>
                  <div class="d-flex align-items-center">
                    <div class="h5 px-3">
                      <i class="fas fa-home"></i>
                    </div>
                    <div>
                      <span class="text-md">Dashboard</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="py-2 my-3 rounded-sm sidelink">
                <div>
                  <div class="d-flex align-items-center">
                    <div class="h5 px-3">
                      <i class="fas fa-users"></i>
                    </div>
                    <div>
                      <span class="text-md">Users</span>
                    </div>
                  </div>
                </div>
              </div>
              <div class="py-2 my-3 rounded-sm sidelink">
                <div>
                  <div class="d-flex align-items-center">
                    <div class="h5 px-3">
                      <i class="fas fa-shopping-bag"></i>
                    </div>
                    <div>
                      <span class="text-md">Products</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </nav>
      <!-- Sidebar -->

      <!-- Navbar -->
      <nav
        id="main-navbar"
        class="
          navbar navbar-expand-lg navbar-light
          fixed-top
          shadow-sm
          navbar-mobile
        "
      >
        <!-- Container wrapper -->
        <div class="container-fluid">
          <div>
            <!-- Toggle button -->
            <button
              class="navbar-toggler"
              type="button"
              data-mdb-toggle="collapse"
              data-mdb-target="#sidebarMenu"
              aria-controls="sidebarMenu"
              aria-expanded="false"
              aria-label="Toggle navigation"
            >
              <i class="fas fa-bars"></i>
            </button>

            <!-- Brand -->
            <a class="navbar-brand" href="#">
              <img
                src="/assets/img/logo.png"
                height="25"
                alt="MDB Logo"
                loading="lazy"
              />
            </a>
          </div>

          <!-- Right links -->
          <ul class="navbar-nav ms-auto d-flex flex-row align-items-center">
            <h6 class="mt-2 pr-1">Selamat Datang, Andi</h6>
            <div>
              <b-dropdown
                size="sm"
                variant="link"
                toggle-class="text-decoration-none"
                no-caret
              >
                <template #button-content>
                  <div class="text-secondary">
                    <span class="h4"><i class="fas fa-user-circle"></i></span>
                    <span class="h6"> <i class="fas fa-caret-down"></i></span>
                  </div>
                </template>
                <b-dropdown-item href="#">Action</b-dropdown-item>
                <b-dropdown-item href="#">Another action</b-dropdown-item>
                <b-dropdown-item href="#"
                  >Something else here...</b-dropdown-item
                >
              </b-dropdown>
            </div>
          </ul>
        </div>
        <!-- Container wrapper -->
      </nav>
      <!-- Navbar -->
    </header>
    <!--Main Navigation-->
    <!--Main layout-->
    <main style="margin-top: 58px; background-color: #f4f6f8; height: 100vh">
      <div class="container py-4">
        <nuxt />
      </div>
    </main>
    <!--Main layout-->
  </div>
</template>

<script>
export default {}
</script>

<style>
@media (min-width: 991.98px) {
  main {
    padding-left: 240px;
  }
}

.text-md {
  font-size: 20px;
  font-weight: 500;
  line-height: 30px;
}

.text-base {
  font-size: 16px;
  font-weight: 500;
}
.text-sm {
  font-size: 14px;
  font-weight: 400;
}

.text-xl {
  font-size: 32px;
  font-weight: 600;
  line-height: 48px;
}

.navbar-mobile {
  background-color: red;
  background-color: #fff;
  z-index: 99;
}
/* Sidebar */
.sidebar {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  padding: 10px 0 0; /* Height of navbar */
  box-shadow: 0 2px 5px 0 rgb(0 0 0 / 5%), 0 2px 10px 0 rgb(0 0 0 / 5%);
  width: 240px;
  z-index: 600;
}
.sidelink {
  color: #fff;
  transition: 0.4s;
}

.sidelink:hover {
  background-color: #fff;
  color: #546fe4;
}

@media (max-width: 991.98px) {
  .sidebar {
    width: 100%;
  }
}
.sidebar .active {
  border-radius: 5px;
  box-shadow: 0 2px 5px 0 rgb(0 0 0 / 16%), 0 2px 10px 0 rgb(0 0 0 / 12%);
}

.sidebar-sticky {
  position: relative;
  top: 0;
  height: calc(100vh - 48px);
  padding-top: 0.5rem;
  overflow-x: hidden;
  overflow-y: auto; /* Scrollable contents if viewport is shorter than content. */
}
</style>