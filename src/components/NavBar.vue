<script setup>
import { RouterLink } from 'vue-router';
import { defineEmits } from 'vue'
const emit = defineEmits(['searchKeyword'])

const emitSearchKeyword = (keyword) => {
    emit("searchKeyword", keyword)
}


</script>
<template>
    <header class="container">
        <div class="nav-links">
            <RouterLink active-class="activeLink" to="/">Home</RouterLink>
            <RouterLink active-class="activeLink" to="/About">About</RouterLink>
        </div>
        <div>
            <h1>Quizes</h1>
            <input type="text" placeholder="Search..." @input="event => emitSearchKeyword(event.target.value)" />
        </div>
    </header>

</template>

<style scoped>
.activeLink {
    font-weight: 700;
    color: rgb(153, 104, 14);
}

header {
    margin-bottom: 10px;
    margin-top: 30px;
    display: flex;
    align-items: center;
}

header h1 {
    font-weight: bold;
    margin-right: 30px;
}

.container {
    width: 100vw;
    margin: 10px;
    padding: 20px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}

.nav-links {
    padding: 20px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
}
</style>,