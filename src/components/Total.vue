<template>
  <span>
    <tr>
      <td></td>
      <td></td>
      <td>
        <b>
          Total Items
        </b>
      </td>
      <td>
        <b>
          Subtotal
        </b>
      </td>
      <td></td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td> {{ totalItems }} </td>
      <td>€{{ subTotal }} </td>
      <td></td>
    </tr>
  </span>
</template>

<script>
export default {
  props: {
    totalItems: Number,
    subTotal: Number,
  },
};
</script>

<style scope>
tr {
  width: 400px;
  display: flex;
  justify-content: space-evenly;
}
td {
  width: 100px;
  text-align: center;
}
</style>
