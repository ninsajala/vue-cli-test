<template>
  <span>
    <tr v-for="(item, index) in cartItems" :key="index">
      <td>{{ item.name }} </td>
      <td>{{ item.price }}</td>
      <td> <input v-model="item.amount" type="number" /> </td>
      <td>{{ item.price * item.amount }} </td>
      <td>
        <b-button variant="danger" @click="cartItems.splice(index, 1)"
          ><i class="fas fa-trash-alt"></i
        ></b-button>
      </td>
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

<style scoped>
tr {
  width: 450px;
  display: flex;
  justify-content: space-evenly;
  height: 50px;
  align-items: center;
}
td {
  width: 100px;
  text-align: center;
}

input {
  width: 40px;
  text-align: center;
}
</style>
