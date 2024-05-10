<script setup>
import { ref } from 'vue'

const users = ["Pepe" ,"Ana", "Juana", "Lola", "Martina"]

const ItsChecked = ref('false')
</script>
<template>
<ul>
    <li v-for="(user, index) in users" :key="index++" > {{ index }} {{ user }}</li>
</ul>



<input type="checkbox" id="checked" v-model="ItsChecked"/>
<label for="checkbox" class="ml-2">{{ ItsChecked }}</label>

<div class="bg-red-400 text-white rounded py-1 px-2 w-24 flex justify-center items-center cursor-default" :class="{'bg-blue-500 font-bold': ItsChecked}">
    Este es un mensaje 
</div>

<div v-if="ItsChecked">
Si
</div>
<div v-else="ItsChecked">
No
</div>
</template>
