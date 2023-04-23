<template>
  <q-page class="row items-center justify-evenly">
    <ExpenseList
      title="Expenses List"
      :expenses="expenses"
     />
  </q-page>
</template>

<script setup lang="ts">
import { Expense } from 'models/expense';
import ExpenseList from 'components/ExpenseList.vue';
import { ref } from 'vue';

const expenses = ref<Expense[]>([
  {
    uid: '1',
    expenditure: 'beer',
    amount: 4000,
    date_created: '2023-03-12',
    date_modified: '2023-03-12'
  },
  {
    uid: '2',
    expenditure: 'sugar',
    amount: 5000,
    date_created: '2023-03-12',
    date_modified: '2023-03-12'
  },
  {
    uid: '3',
    expenditure: 'water',
    amount: 2200,
    date_created: '2023-03-12',
    date_modified: '2023-03-12'
  },
]);
</script>
