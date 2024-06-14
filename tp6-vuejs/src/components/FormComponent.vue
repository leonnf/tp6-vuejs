<template>
    <form @submit.prevent="handleSubmit">
        <div>
            <label for="username">Username:</label>
            <input type="text" id="username" v-model="username" />
        </div>
        <div>
            <label for="password">Password:</label>
            <input type="password" id="password" v-model="password" />
        </div>
        <div>
            <label for="email">Email:</label>
            <input type="email" id="email" v-model="email" />
        </div>
        <div>
            <input type="submit" value="Enviar" />
        </div>
    </form>
</template>
  
<script setup lang="ts">
import { ref, Ref } from 'vue'

const username: Ref<string> = ref('')
const password: Ref<string> = ref('')
const email: Ref<string> = ref('')
const enviar: Ref<string> = ref('')

function handleSubmit() {
    console.log('Username:', username.value)
    console.log('Password:', password.value)
    console.log('Email:', email.value)
    console.log('Enviar:', enviar.value)
}
</script>
  
<style scoped>
/* Estilos CSS */
body {
    background-color: #2e2e2e;

    color: #f8f8f2;

    font-family: 'Courier New', Courier, monospace;

}

form {
    background-color: #3e3e3e;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    max-width: 400px;
    margin: 50px auto;
}

label {
    display: block;
    margin-bottom: 10px;
    color: #50fa7b;

}

input[type="text"],
input[type="password"],
input[type="email"],
input[type="submit"] {
    display: block;
    width: calc(100% - 24px);
    padding: 10px;
    margin-bottom: 20px;
    border: 2px solid #6272a4;
    border-radius: 4px;
    background-color: #282a36;
    color: #f8f8f2;
}

input[type="submit"] {
    display: block;
    margin: 0 auto;
    background-color: #ff79c6;
    border: none;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.3s;
}

input[type="submit"]:hover {
    background-color: #000000;
}
</style>
  
