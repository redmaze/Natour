<template>
    <main>
        <About />
        <Feature />
        <Tours />
        <Stories />
        <Book />
    </main>
</template>

<script>
import About from './section/About.vue'
import Book from './section/Book.vue'
import Feature from './section/Feature.vue'
import Stories from './section/Stories.vue'
import Tours from './section/Tours.vue'

export default {
  name: 'Main',
  components: {
    About,
    Book,
    Feature,
    Stories,
    Tours
  }
}
</script>
