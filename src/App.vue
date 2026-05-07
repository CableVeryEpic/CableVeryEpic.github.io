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
        <h1>Welcome to my portfolio!</h1>
        <p>This is a collection of various projects I've worked on and mostly completed. Some are from uni, some are personal projects.</p>
    </header>

    <main>
        <div class="showcase-container">
            <div class="showcase-page">
                <div class="showcase-right">
                    <h3>Tools</h3>
                    <p>Here are some tools I've made, click on them to learn more!</p>
                </div>
                <div class="showcase-left">
                    <a href="https://github.com/CableVeryEpic/KIT205_466399" target="_blank">
                        <img src="https://opengraph.githubassets.com/astar/CableVeryEpic/KIT205_466399" alt="Tool Image" width="50%">
                    </a>
                </div>
                
            </div>
        </div>
        <div class="showcase-container">
            <div class="showcase-page">
                <div class="showcase-right">
                    <h3>Games</h3>
                    <p>Here are some games I've made, click on them to play!</p>
                </div>
                <div class="showcase-left">
                    <iframe width="552" height="167" frameborder="0" src="https://itch.io/embed/2641546"><a href="https://cablel.itch.io/grave-mistakes">Grave Mistakes by Cablel</a></iframe>
                    <iframe height="167" frameborder="0" width="552" src="https://itch.io/embed/2759969"><a href="https://cablel.itch.io/desert-golf">Desert Golf by Cablel</a></iframe>
                </div>
                
            </div>
        </div>
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
