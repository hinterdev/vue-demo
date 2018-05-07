<template>
  <div class="">
    <input type="text" v-model="inputValue">
    <button type="button" name="button" @click="handleSubmit">Submit</button>
    <ul>
        <li v-for="(item, index) of list" :key="index"  :index="index" @click="handleDelete(index)">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
    data () {
        return {
            inputValue: '',
            list: []
        }
    },
    methods: {
        handleSubmit () {
            this.list.push(this.inputValue)
            this.inputValue = ''
        },
        handleDelete (index) {
            this.list.splice(index, 1)
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
