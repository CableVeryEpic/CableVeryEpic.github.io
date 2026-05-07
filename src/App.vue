<script setup>
import { ref } from 'vue'

const page = ref(0);

function incrementPage() {
    page.value = (page.value + 1) % 5;
}

function decrementPage() {
    page.value = (page.value - 1 + 5) % 5;
}
</script>

<template>
    <header>

    </header>

    <main>
        <div class="showcase-container">
            <div class="showcase-page">
                <div class="showcase-details">
                    <h3>Scrolling City</h3>
                    <p>A simple scrolling city simulation</p>
                </div>
                <iframe v-if="page === 0" src="https://editor.p5js.org/Cable/full/q_0I7APQO" width="600" height="442"></iframe>
                <iframe v-else-if="page === 1" src="https://editor.p5js.org/Cable/full/9tTDfqzss" width="600" height="742"></iframe>
                <iframe v-else-if="page === 2" src="https://editor.p5js.org/Cable/full/60KIhZOB4" width="1280" height="785"></iframe>
                <iframe v-else-if="page === 3" src="https://editor.p5js.org/Cable/full/4tppHknc1" width="800" height="842"></iframe>
                <iframe v-else-if="page === 4" src="https://editor.p5js.org/Cable/full/avKP3dxo" width="300" height="326"></iframe>
            </div>
            <div class="showcase-nav">
                <button @click="decrementPage">Previous</button>
                page {{ page + 1 }} / 5
                <button @click="incrementPage">Next</button>
            </div>
        </div>
    </main>

    <footer></footer>
</template>

<style scoped>
</style>
