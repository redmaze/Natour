<template>
    <div class="col-1-of-3">
        <div class="card">
            <div class="card__side card__side--front">
                <div :class="['card__picture', `card__picture--${id}`]">
                    &nbsp;
                </div>
                <h4 class="card__heading">
                    <span :class="['card__heading-span', `card__heading-span--${id}`]">{{title}}</span>
                </h4>
                <div class="card__details">
                    <ul>
                        <li v-for='(perk, idx) in perks' :key='idx'>{{perk}}</li>
                    </ul>
                </div>
            </div>
            <div :class="['card__side', 'card__side--back', `card__side--back-${id}`]">
                <div class="card__cta">
                    <div class="card__price-box">
                        <p class="card__price-only">Only</p>
                        <p class="card__price-value">{{price}}</p>
                    </div>
                    <a href="#popup" class="btn btn--white">Book now!</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Spinning-Card',
  props: [
    'title',
    'id',
    'price',
    'perks'
  ]
}
</script>
