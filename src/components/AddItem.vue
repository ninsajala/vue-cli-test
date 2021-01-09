<template>
  <form >
    <input type="text" :newItem="newItem.name"/>
    <input type="number" :newItem="newItem.price" />
    <input type="number" :newItem="newItem.amount" />
    <button @click.prevent="addItem">Add</button>
  </form>
</template>

<script>
export default {
  props: {
    newItem: Object,
    addItem: Function,
  },
};
</script>
