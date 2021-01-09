<template>
  <span>
    <tr>
      <td></td>
      <td></td>
      <td> {{ totalItems }} </td>
      <td>SubTotal{{ subTotal }} </td>
    </tr>
  </span>
</template>

<script>
export default {
  props: {
    totalItems: Function,
    subTotal: Function,
  },
};
</script>
