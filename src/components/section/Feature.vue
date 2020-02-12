<template>
    <section class="section-features">
        <div class="row">
            <FeatureCard
                v-for="(feature, idx) in features"
                :key="idx"
                :title="feature.title"
                :icon="feature.icon"
                :text="feature.text" />
        </div>
    </section>
</template>

<script>
import FeatureCard from '@/components/card/FeatureCard'

export default {
  name: 'Feature-Section',
  components: {
    FeatureCard
  },
  data () {
    return {
      features: [
        {
          icon: 'icon-basic-world',
          title: 'Explore the world',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente aspernatur.'
        },
        {
          icon: 'icon-basic-compass',
          title: 'Meet nature',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente aspernatur.'
        },
        {
          icon: 'icon-basic-map',
          title: 'Find your way',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente aspernatur.'
        },
        {
          icon: 'icon-basic-heart',
          title: 'Live a healthier life',
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente aspernatur.'
        }
      ]
    }
  }
}
</script>
