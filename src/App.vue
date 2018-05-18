<template>
    <div id="app">
        <TodoList/>
        <div>
            {{content}}
        </div>
    </div>
</template>

<script>
import TodoList from './components/TodoList'
import './js/_demo.js'
export default {
    name: 'App',
    components: {
        TodoList
    },
    data () {
        return {
            content: 'Hello World!'
        }
    },
    mounted () {
        this.setContent()
    },
    methods: {
        setContent: function () {
            let _this = this
            setTimeout(function () {
                _this.content = 'Bye'
            }, 2000)
        }
    }
}
</script>

<style lang="scss">

</style>
