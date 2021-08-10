<template>
  <div>
    <h1 class="mb-8">Список задач</h1>
    <wrapper-block class="text-sm font-medium overflow-x-auto h-5/6">
      <div class="flex justify-between">
        <div class="todo-header__title">Задача</div>
        <div class="todo-header__title">Статус</div>
      </div>
      <div class="todo-lists">
        <div
          class="todo-lists__item flex justify-between"
          v-for="(todo, i) in todos"
          :key="i"
        >
          <div class="item__text">{{todo.title}}</div>
          <div class="item__status flex items-center">
            <input checked type="checkbox" :id="todo.id" class="mr-2">
            <label :for="todo.id">Выполнено</label>
          </div>
        </div>
      </div>
    </wrapper-block>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import WrapperBlock from '@/components/blocks/wrapperContent'

export default {
  layout: 'rootlayout',
  components: {
    WrapperBlock
  },
  computed: {
    ...mapGetters({
      todos: 'todos/allTodos'
    })
  },
  async mounted () {
    await this.$store.dispatch('todos/fetchTodos')
  }
}
</script>

<style lang="scss" scoped>
.todo-header__title {
  color: #BABABA;
  font-weight: 500;
}

.todo-lists__item {
  padding: 16px 0;
  border-top: 1px solid #EFF1F9;
  border-bottom: 1px solid #EFF1F9;
}
</style>
