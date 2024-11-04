<script setup>
const sayHello = () => console.log("Hello")
const counter = useCounter();

const response = await $fetch('/api/hello')
console.log(response)
</script>

<template>
    <div class="Main" >
        <div id="main">
        <Alert />
        <Profile />
        <img src="/1.png" alt="" />

        Counter: {{ counter }}
        <button @click="counter++">
            +
        </button>
        <button @click="counter--">
            -
        </button>
        <Counter id="counter"/>
        </div>
    </div>
</template>