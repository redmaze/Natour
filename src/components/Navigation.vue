<template>
    <div class="navigation">
        <input type="checkbox" class="navigation__checkbox" id="navi-toggle">

        <label for="navi-toggle" class="navigation__button">
            <span class="navigation__icon">&nbsp;</span>
        </label>

        <div class="navigation__background">&nbsp;</div>

        <nav class="navigation__nav">
            <ul class="navigation__list">
                <li
                    class="navigation__item"
                    v-for="(route, idx) in routes"
                    :key="idx"
                >
                    <a :href="route.link" class="navigation__link">
                        <span>0{{idx}}</span>{{route.text}}
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
  name: 'Navigation',
  data () {
    return {
      routes: [
        {
          link: '#',
          text: 'About Natours'
        },
        {
          link: '#',
          text: 'Your Benefits'
        },
        {
          link: '#',
          text: 'Popular Tours'
        },
        {
          link: '#',
          text: 'Stories'
        },
        {
          link: '#',
          text: 'Book Now!'
        }
      ]
    }
  }
}
</script>
