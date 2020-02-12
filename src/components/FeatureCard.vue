<template>
    <div class="col-1-of-4">
        <div class="feature-box">
            <i :class="['feature-box__icon', icon || 'icon-basic-world']"></i>
            <h3 class="heading-tertiary u-margin-bottom-small">{{ title }}</h3>
            <p class="feature-box__text">
                {{ text }}
            </p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Feature-Card',
  props: ['title', 'icon', 'text']
}
</script>
