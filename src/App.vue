<template>
  <div id="app" class="shoppingCart">
    <table>
      <thead>
        <tr>
          <th>Item</th>
          <th>Price</th>
          <th>Amount</th>
          <th>Total</th>
        </tr>
      </thead>
      <tbody>
        <CartItems :cartItems="cartItems" />
        <Total :subTotal="subTotal" :totalItems="totalItems" />
      </tbody>
    </table>
    <AddItem :newItem="newItem" :addItem="addItem" />
  </div>
</template>

<script>
import CartItems from './components/CartItems.vue';
import AddItem from './components/AddItem.vue';
import Total from './components/Total.vue';

export default {
  name: 'App',
  components: {
    CartItems,
    AddItem,
    Total,
  },
  data() {
    return {
      newItem: {
        name: '',
        price: 0,
        amount: 0,
      },
      cartItems: [
        {
          name: 'Zaklamp',
          price: 4.5,
          amount: 2,
        },
        {
          name: 'Wijnglas',
          price: 5.85,
          amount: 1,
        },
      ],
    };
  },
  methods: {
    addItem() {
      this.cartItems.push(this.newItem);
      this.newItem = { name: '', price: 0, amount: 0 };
    },
  },
  computed: {
    subTotal() {
      let total = 0;
      this.cartItems.forEach((item) => (total += item.price * item.amount));
      return total;
    },
    totalItems() {
      let totalAmount = 0;
      this.cartItems.forEach((item) => (totalAmount += item.amount));
      return totalAmount;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

table {
  border: 2px solid black;
}

tr {
  width: 400px;
}

th {
  width: 50px;
}
</style>
