<template>
  <div>
    <form @submit.prevent>
      <input type="text" v-model="inputValue">
      <button @click="handClick">提交</button>
    </form>
    <ul>
      <todo-item v-for='(item , index) of list' :content="item" :key="index" :index="index" @delete="deleteClick"></todo-item>
    </ul>
  </div>
</template>

<script>
import todoItem from './components/todoItem.vue'

export default {
  components: {
    'todo-item': todoItem
  },
  data () {
    return {
      inputValue: '',
      list: []
    }
  },
  methods: {
    handClick () {
      if (this.inputValue) {
        this.list.push(this.inputValue)
        this.inputValue = ''
      } else {
        alert('提交不能为空')
      }
    },
    deleteClick (index) {
      this.list.splice(index, 1)
    }
  }
}
</script>

<style>

</style>
