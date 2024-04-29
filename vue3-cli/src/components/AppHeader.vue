<template>
    <h1>{{ appTitle }}</h1>
    <!-- v-on:click은 @click으로 축약 가능 -->
    <button @click="changeTitle">변경</button>
</template>

<script>
    export default {
        props: ['appTitle'],
        methods: {
            changeTitle() {
                this.$emit('change')
            }
        }
    }
</script>

<style scoped>

</style>