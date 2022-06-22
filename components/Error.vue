<template>
  <div>
    <div class="container py-5 h-100">
      <div class="row d-flex justify-content-center align-items-center h-100">
        <div class="col-12 col-md-8 col-lg-6 col-xl-5">
          <div class="card py-4 rounded-lg">
            <img
              src="/assets/img/warning_illustration.png"
              alt=""
              style="width: 55%; margin: 0 auto"
            />
            <div class="card-body py-4 text-center">
              <section class="py" style="width: 80%; margin: 0 auto">
                <form>
                  <h5 class="mb-4" style="font-weight: 500; color: #88888A;">
                    We’re sorry, the page you requested could not be found.
                    Please go back to the homepage
                  </h5>

                  <div class="form-group">
                    <button
                      type="submit"
                      class="btn btn-block text-white py-2 rounded-md login-btn"
                    >
                      Home
                    </button>
                  </div>
                  <!-- form-group// -->
                </form>
              </section>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.login-btn {
  background-color: #3252df;
  box-shadow: 1px 4px 8px rgba(50, 82, 223, 0.3);
}
.login-btn:hover {
  background-color: #3564dc;
  box-shadow: 1px 7px 8px rgba(50, 82, 223, 0.3);
}

.input-group .icon-addon .form-control {
  border-radius: 0;
}

.icon-addon {
  position: relative;
  color: #b0b0b0;
  display: block;
}

.icon-addon:after,
.icon-addon:before {
  display: table;
  content: ' ';
}

.icon-addon:after {
  clear: both;
}

.icon-addon.addon-md .glyphicon,
.icon-addon .glyphicon,
.icon-addon.addon-md .fa,
.icon-addon .fa {
  position: absolute;
  z-index: 2;
  left: 10px;
  font-size: 14px;
  width: 20px;
  margin-left: -2.5px;
  text-align: center;
  padding: 10px 0;
  top: 5px;
}

.icon-addon.addon-lg .form-control {
  line-height: 1.33;
  height: 46px;
  font-size: 18px;
  padding: 10px 16px 10px 40px;
}
</style>