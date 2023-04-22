<template>
  <div>
    <h4>{{ title }}</h4>
    <ul>
      <li v-for="expense in expenses" :key="expense.uid">
        {{ expense.uid }} - {{ expense.expenditure }} - {{ expense.amount}}
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue';
import { Expense } from 'models/expense';

interface Props {
  title: string;
  expenses?: Expense[];
}
const props = withDefaults(defineProps<Props>(), {
  todos: () => [],
});

const clickCount = ref(0);
function increment() {
  clickCount.value += 1;
  return clickCount.value;
}

const todoCount = computed(() => props.todos.length);

</script>
