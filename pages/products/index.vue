<template>
  <div class="container">
    <b-breadcrumb
      style="background-color: #f4f6f8; margin-left: -15px"
      :items="items"
    ></b-breadcrumb>
    <div class="text-xl">Overview Stock Pulsa</div>
    <div class="my-4">
      <ListGroup />
    </div>

    <DataTableProduct />
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          text: 'Dashboard',
          href: '#',
        },
        {
          text: 'Product',
          href: '#',
        },
        {
          text: 'Pulsa',
          active: true,
        },
      ],
    }
  },
}
</script>