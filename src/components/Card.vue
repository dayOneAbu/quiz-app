<script setup>

const { quiz } = defineProps(['quiz'])

</script>
<template>
    <RouterLink class="link-text" :to="`/quiz/${quiz.id}`">
        <div class="card">
            <img :src="quiz.img" alt="">
            <div>
                <h2>{{ quiz.name }}</h2>
                <p>{{ quiz.questions.length }} questions</p>
            </div>
        </div>
    </RouterLink>

</template>
<style scoped>
/* CARD */

.card {
    width: 310px;
    overflow: hidden;
    border-radius: 2%;
    box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 35px;
    margin-right: 20px;
    cursor: pointer;
}

.card img {
    width: 100%;
    height: 190px;
    margin: 0
}

.link-text {
    padding: 0 5px;
    font-weight: bold;
    color: orange;
}

.card .card-text h2 {
    padding: 0 5px;
    font-weight: bold;
}
</style>