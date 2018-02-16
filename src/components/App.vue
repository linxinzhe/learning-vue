<template>
    <div>
        <componentA></componentA>
        <ul>
            <li v-for="item in list">{{item.name }} - {{item.age}}</li>
        </ul>
        {{hello}}
        <button v-on:click="addItem">addItem</button>
    </div>
</template>

<script>
    import componentA from "./A.vue"

    export default {
        name: "app",
        components: {
            componentA: componentA
        },
        data() {
            return {
                hello: 'hello test world',
                list: [
                    {name: "linxinzhe", age: 20},
                    {name: "denglingfeng", age: 22},
                ],
                objList: {
                    name: "laolin",
                    age: 11,
                    classroom: "room2"
                }
            }
        },
        methods: {
            addItem() {
                this.list.push({
                    name: "laoli", age: 44
                })
            }
        }
    }
</script>

<style scoped>
    html {
        height: 100%;
    }
</style>