<template>
  <div class="container">
    <div class="text-xl mb-3">Users Management</div>
    <DataTable />
  </div>
</template>
<script>
import DataTable from '@/components/DataTable.vue'
export default {
  components: {
    DataTable,
  },
  data() {
    return {
      items: [{}, {}],
    }
  },
}
</script>