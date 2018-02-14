<template>
    <div>
        {{hello}}
    </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
                hello: 'hello test world'
            }
        }
    }
</script>

<style scoped>
    html {
        height: 100%;
    }
</style>