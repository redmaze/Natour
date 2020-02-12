<template>
    <footer class="footer">
        <div class="footer__logo-box">
            <picture class="footer__logo">
                <img alt="Full logo" :src="require('@/assets/img/logo-green-2x.png')">
            </picture>
        </div>
        <div class="row">
            <div class="col-1-of-2">
                <div class="footer__navigation">
                    <ul class="footer__list">
                        <li
                            class="footer__item"
                            v-for="(route, idx) in routes"
                            :key="idx">
                            <a :href="route.link" class="footer__link">{{route.text}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-1-of-2">
                <p class="footer__copyright">
                    Built by <a href="#" class="footer__link">Jonas Schmedtmann</a> for his online course <a href="#" class="footer__link">Advanced CSS and Sass</a>.
                    Copyright &copy; by Jonas Schmedtmann. You are 100% allowed to use this webpage for both personal
                    and commercial use, but NOT to claim it as your own design. A credit to the original author, Jonas
                    Schmedtmann, is of course highly appreciated!
                </p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
  name: 'Navigation',
  data () {
    return {
      routes: [
        {
          link: '#',
          text: 'Company'
        },
        {
          link: '#',
          text: 'Contact Us'
        },
        {
          link: '#',
          text: 'Careers'
        },
        {
          link: '#',
          text: 'Privacy Policy'
        },
        {
          link: '#',
          text: 'Terms'
        }
      ]
    }
  }
}
</script>
