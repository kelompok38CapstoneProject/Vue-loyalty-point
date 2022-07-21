<template>
  <div>
    <div class="container py-5 h-100">
      <div class="row d-flex justify-content-center align-items-center h-100">
        <div class="col-12 col-md-8 col-lg-6 col-xl-5">
          <div class="card py-4 rounded-lg">
            <img
              src="/assets/img/logoo.png"
              alt=""
              style="width: 35%; margin: 0 auto"
            />
            <div class="card-body py-4 text-center">
              <section class="py-5" style="width: 80%; margin: 0 auto">
                <form>
                  <h4 class="mb-4" style="font-weight: 600">Admin Login</h4>
                  <div class="form-group">
                    <div class="icon-addon addon-lg">
                      <input
                        type="text"
                        style="background-color: #f4f6f8; border: none"
                        placeholder="Username"
                        class="form-control"
                        v-model="frm.email"
                        id="email"
                      />
                      <i class="fas fa-user glyphicon"></i>
                    </div>
                  </div>
                  <div class="form-group">
                    <div class="icon-addon addon-lg">
                      <input
                        type="password"
                        style="background-color: #f4f6f8; border: none"
                        placeholder="Password"
                        class="form-control"
                        v-model="frm.password"
                        id="password"
                      />
                      <i class="fas fa-key glyphicon"></i>
                    </div>
                  </div>

                  <div class="form-group">
                    <button
                      @click.prevent="doLogin"
                      type="submit"
                      class="btn btn-block text-white py-2 rounded-md login-btn"
                    >
                      Masuk
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
export default {
  data() {
    return {
      frm: {
        email: 'adminpoint1@gmail.com',
        password: '',
      },
    }
  },
  mounted() {},
  methods: {
    async doLogin() {
      try {
        let rs = await this.$axios.post('login/admin', this.frm)
        console.log(rs)
        let { data } = rs
        localStorage.setItem('user', JSON.stringify(data))
        localStorage.setItem('token', JSON.stringify(data.token))
        this.$toast('Ok')
        this.$router.push('/')
      } catch (error) {
        this.$toast.error('Password salah')
      }
    },
  },
}
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