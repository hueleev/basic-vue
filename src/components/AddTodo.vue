<template>
    <input
        v-model="todoText"
        type="text"
        class="w-100 p-2"
        placeholder="type TODO"
        @keyup.enter="addTodo"/>
</template>

<script>
    export default {
        data() {
            return {
                todoText: ''
            }
        },
        methods: {
            addTodo(e) {
                /* this.$store.commit('ADD_TODO', e.target.value); */
                this.$store.dispatch('todo/addTodo', e.target.value)
                this.todoText = '';
            }
        }
    }
</script>

<style></style>