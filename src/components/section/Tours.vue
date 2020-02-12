<template>
    <section class="section-tours" id="section-tours">
        <div class="u-center-text u-margin-bottom-big">
            <h2 class="heading-secondary">
                Most popular tours
            </h2>
        </div>
        <div class="row">
            <SpinningCard
                v-for="(tour, id) in tours"
                :key="id"
                :title="tour.title"
                :id="id+1"
                :price="tour.price"
                :perks="tour.perks"
            />
        </div>

        <div class="u-center-text u-margin-top-huge">
            <a href="#" class="btn btn--green">Discover all tours</a>
        </div>
    </section>
</template>

<script>
import SpinningCard from '@/components/card/SpinningCard'

export default {
  name: 'Tours-Section',
  components: {
    SpinningCard
  },
  data () {
    return {
      tours: [
        {
          title: 'The Sea Explorer',
          price: '$297',
          perks: [
            '3 day tours',
            'Up to 30 people',
            '2 tour guides',
            'Sleep in cozy hotels',
            'Difficulty: easy'
          ]
        },
        {
          title: 'The Forest Hiker',
          price: '$497',
          perks: [
            '3 day tours',
            'Up to 30 people',
            '2 tour guides',
            'Sleep in cozy hotels',
            'Difficulty: easy'
          ]
        },
        {
          title: 'The Snow Adventurer',
          price: '$897',
          perks: [
            '3 day tours',
            'Up to 30 people',
            '2 tour guides',
            'Sleep in cozy hotels',
            'Difficulty: easy'
          ]
        }
      ]
    }
  }
}
</script>
