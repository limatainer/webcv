
<script setup lang="ts">
import ThemeToggle from "../../../components/ThemeToggle.vue"
</script>

<template>
    <nav class="flex justify-between p-4 items-center border-b">
        <div>
            <img src="/logo.png" alt="" class="w-46 object-contain">
        </div>
        <ul class="flex font-semibold text-lg gap-10 ">
            <li class="list-item">Home</li>
            <li class="list-item">Skills</li>
            <li class="list-item">Projects</li>
            <li class="list-item">Certificates</li>
        </ul>
        <button class="bg-primary text-white px-6 py-2 rounded-lg cursor-pointer hover:bg-primary/70 mr-16">
         Let's Connect
        </button>
        <ThemeToggle />
   </nav>
</template>

<style scoped>
.list-item {
    cursor: pointer;
    transition: color 0.3s ease;
}
.list-item:hover {
    color: var(--primary);
    border-bottom: 2px solid var(--primary);
}
</style>