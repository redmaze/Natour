<template>
    <div class="row">
        <div class="story">
            <figure class="story__shape">
                <img :src="require(`@/assets/img/${img}`)" alt="Person on a tour" class="story__img">
                <figcaption class="story__caption">{{name}}</figcaption>
            </figure>
            <div class="story__text">
                <h3 class="heading-tertiary u-margin-bottom-small">{{title}}</h3>
                    <p>
                        {{text}}
                    </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Story-Card',
  props: ['name', 'title', 'text', 'img']
}
</script>
