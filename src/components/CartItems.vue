<template>
  <span>
    <tr v-for="(item, index) in cartItems" :key="index">
      <td>{{ item.name }} </td>
      <td>{{ item.price }}</td>
      <td> {{ item.amount }} </td>
      <td>{{ item.price * item.amount }} </td>
    </tr>
  </span>
</template>

<script>
export default {
  props: {
    cartItems: Array,
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
  width: 50px;
}
</style>
