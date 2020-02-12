<template>
    <section class="section-stories">
        <div class="bg-video">
            <video class="bg-video__content" autoplay muted loop>
                <source :src="require('@/assets/img/video.mp4')" type="video/mp4">
                <source :src="require('@/assets/img/video.webm')" type="video/webm">
                Your browser is not supported!
            </video>
        </div>

        <div class="u-center-text u-margin-bottom-big">
            <h2 class="heading-secondary">
                We make people genuinely happy
            </h2>
        </div>

        <StoryCard
            v-for='(story, idx) in stories'
            :key="idx"
            :title="story.title"
            :img="story.img"
            :text="story.text"
            :name="story.name"
        />

        <div class="u-center-text u-margin-top-huge">
            <a href="#" class="btn-text">Read all stories &rarr;</a>
        </div>
    </section>
</template>

<script>
import StoryCard from '@/components/card/StoryCard'

export default {
  name: 'Story-Section',
  components: {
    StoryCard
  },
  async mounted () {
    //   let response = await getStories();
    //   this.stories = response.data;
  },
  data () {
    return {
      stories: [
        {
          img: 'nat-8.jpg',
          name: 'Mary Smith',
          title: 'I had the best week ever with my family',
          text: `
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente aspernatur libero repellat quis consequatur
            ducimus quam nisi exercitationem omnis earum qui. Aperiam, ipsum sapiente aspernatur libero
            repellat quis consequatur ducimus quam nisi exercitationem omnis earum qui.
            `
        },
        {
          img: 'nat-9.jpg',
          name: 'Jack Wilson',
          title: 'WOW! My life is completely different now',
          text: `
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, ipsum sapiente aspernatur libero repellat quis consequatur
            ducimus quam nisi exercitationem omnis earum qui. Aperiam, ipsum sapiente aspernatur libero
            repellat quis consequatur ducimus quam nisi exercitationem omnis earum qui.
            `
        }
      ]
    }
  }
}
</script>
