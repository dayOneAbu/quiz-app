<script setup>
import { ref, watch } from 'vue'
import { RouterLink } from 'vue-router';

const search = ref('')

watch(search, () => {
    quizzes.value = quiz_data.filter(quiz => quiz.name.toLowerCase().includes(search.value.toLowerCase()))
})
</script>
<template>
    <header class="container">
        <div class="nav-links">
            <RouterLink active-class="activeLink" to="/">Home</RouterLink>
            <RouterLink active-class="activeLink" to="/About">About</RouterLink>
        </div>
        <div>
            <h1>Quizes</h1>
            <input v-model.trim='search' type="text" placeholder="Search...">
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