<template>
  <div class="container">
    <b-breadcrumb
      style="background-color: #f4f6f8"
      :items="items"
    ></b-breadcrumb>
    <div class="text-xl">Overview Stock Pulsa</div>
    <div class="my-4">
      <ListGroup />
    </div>

    <DataTable />
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