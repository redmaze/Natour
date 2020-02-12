<template>
    <section class="section-book">
        <div class="row">
            <div class="book">
                <div class="book__form">
                    <form action="#" class="form">
                        <div class="u-margin-bottom-medium">
                            <h2 class="heading-secondary">
                                Start booking now
                            </h2>
                        </div>

                        <div class="form__group">
                            <input
                                v-model="name"
                                type="text"
                                class="form__input"
                                placeholder="Full name"
                                id="name" required>
                            <label for="name" class="form__label">Full name</label>
                        </div>

                        <div class="form__group">
                            <input
                                v-model="email"
                                type="email"
                                class="form__input"
                                placeholder="Email address"
                                id="email" required>
                            <label for="email" class="form__label">Email address</label>
                        </div>

                        <div class="form__group u-margin-bottom-medium">
                            <div class="form__radio-group">
                                <input type="radio" class="form__radio-input" id="small" name="size" value="0" v-model="size">
                                <label for="small" class="form__radio-label">
                                    <span class="form__radio-button"></span>
                                    Small tour group
                                </label>
                            </div>

                            <div class="form__radio-group">
                                <input type="radio" class="form__radio-input" id="large" name="size" value="1" v-model="size">
                                <label for="large" class="form__radio-label">
                                    <span class="form__radio-button"></span>
                                    Large tour group
                                </label>
                            </div>
                        </div>

                        <div class="form__group">
                            <button class="btn btn--green">Next step &rarr;</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  name: 'Book-Section',
  data () {
    return {
      name: '',
      email: '',
      size: 0
    }
  },
  watch: {
    size () {
      this.size = parseInt(this.size)
    }
  }
}
</script>
