<template>
  <div class="container">
    <div class="text-xl mb-3">Users Management</div>
    <DataTableUsers />
  </div>
</template>
<script>
import DataTableUsers from '@/components/DataTableUsers.vue'
export default {
  components: {
    DataTableUsers,
  },
  data() {
    return {
      items: [{}, {}],
    }
  },
}
</script>