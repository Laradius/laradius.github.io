<template>
  <q-page class="row justify-evenly">
    <div>
      <div class="col"><PortfolioText /></div>
      <div class="col">
        <PortfolioAvatar />
      </div>
    </div>
  </q-page>
</template>

<script setup lang="ts">
import { Todo, Meta } from 'components/models';
import PortfolioText from 'src/components/PortfolioText.vue';
import PortfolioAvatar from 'src/components/PortfolioAvatar.vue';
import { ref } from 'vue';

const todos = ref<Todo[]>([
  {
    id: 1,
    content: 'ct1',
  },
  {
    id: 2,
    content: 'ct2',
  },
  {
    id: 3,
    content: 'ct3',
  },
  {
    id: 4,
    content: 'ct4',
  },
  {
    id: 5,
    content: 'ct5',
  },
]);
const meta = ref<Meta>({
  totalCount: 1200,
});
</script>
