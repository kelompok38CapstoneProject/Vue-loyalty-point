<template>
  <div class="container">
    <span class="text-xl">Dashboard</span>
    <!-- {{ dataUser }} -->
    <section>
      <DashboardCard />
      <DataTable />
    </section>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      dataUser: [],
    }
  },
  mounted() {
    this.getDataUser()
  },
  methods: {
    async getDataUser() {
      let rs = await this.$axios.get('users/role/admin')
      this.dataUser = rs.data
      console.log(rs)
    },
  },
}
</script>
