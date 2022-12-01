<script setup>
import { ref } from 'vue'
import quiz_data from '../data/quizes_data.json'
import Card from '../components/Card.vue'
const quizzes = ref(quiz_data)

</script>
<template>
    <div class="container">
        <div class="options-container">
            <Card :key="quiz.id" v-for="quiz in quizzes" :quiz=quiz />
        </div>
    </div>
</template>


<style scoped>
.container {
    max-width: 1000px;
    margin: 0 auto
}


header input {
    border: none;
    background-color: rgba(128, 128, 128, 0.1);
    padding: 10px;
    border-radius: 5px;
}

.options-container {
    display: flex;
    flex-wrap: wrap;
    margin-top: 40px;
}
</style>