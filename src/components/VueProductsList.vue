<template>
<div class="main__productsList">
    <VueProductCard v-for="product in productsList" :product="product" :key="product.id"/>    
</div>
</template>

<script>
import VueProductCard from './VueProductCard.vue'

export default {
  name: 'VueProductsList',
  components: {
    VueProductCard
  },
  props: {
  },
  data() {
    return {
        productsList: [
            {
                brand: 'Бренд',
                discount: '25%',
                isBestSeller: true,
                isInStock: false,
                name: 'Полное название товара в несколько строк для вида с обрывом в концe Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae id incidunt quos suscipit dolor quis. Magnam nesciunt voluptatum pariatur repellat quibusdam iste voluptatibus praesentium nihil voluptates? Amet vero saepe earum!',
                currentPrice: '5 990 ₽',
                oldPrice: '5 990 ₽',
            },
            {
                brand: 'Бренд',
                discount: '12%',
                isBestSeller: true,
                isInStock: false,
                name: 'Полное название товара в несколько строк для вида с обрывом в концe Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae id incidunt quos suscipit dolor quis. Magnam nesciunt voluptatum pariatur repellat quibusdam iste voluptatibus praesentium nihil voluptates? Amet vero saepe earum!',
                currentPrice: '5 990 ₽',
                oldPrice: '55 990 ₽'
            },
            {
                brand: 'Бренд',
                discount: '54%',
                isBestSeller: true,
                isInStock: true,
                name: 'Полное название товара в несколько строк для вида с обрывом в концe Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae id incidunt quos suscipit dolor quis. Magnam nesciunt voluptatum pariatur repellat quibusdam iste voluptatibus praesentium nihil voluptates? Amet vero saepe earum!',
                currentPrice: '5 990 ₽',
                oldPrice: '7 990 ₽'
            },
            {
                brand: 'Бренд',
                discount: '0%',
                isBestSeller: true,
                isInStock: true,
                name: 'Полное название товара в несколько строк для вида с обрывом в концe Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae id incidunt quos suscipit dolor quis. Magnam nesciunt voluptatum pariatur repellat quibusdam iste voluptatibus praesentium nihil voluptates? Amet vero saepe earum!',
                currentPrice: '5 990 ₽',
                oldPrice: ''
            },
            {
                brand: 'Бренд',
                discount: '25%',
                isBestSeller: true,
                isInStock: false,
                name: 'Полное название товара в несколько строк для вида с обрывом в концe Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae id incidunt quos suscipit dolor quis. Magnam nesciunt voluptatum pariatur repellat quibusdam iste voluptatibus praesentium nihil voluptates? Amet vero saepe earum!',
                currentPrice: '5 990 ₽',
                oldPrice: '4 990 ₽'
            },
            {
                brand: 'Бренд',
                discount: '25%',
                isBestSeller: false,
                isInStock: true,
                name: 'Полное название товара в несколько строк для вида с обрывом в концe Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae id incidunt quos suscipit dolor quis. Magnam nesciunt voluptatum pariatur repellat quibusdam iste voluptatibus praesentium nihil voluptates? Amet vero saepe earum!',
                currentPrice: '5 990 ₽',
                oldPrice: '5 990 ₽'
            },
            {
                brand: 'Бренд',
                discount: '25%',
                isBestSeller: true,
                isInStock: true,
                name: 'Полное название товара в несколько строк для вида с обрывом в концe Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vitae id incidunt quos suscipit dolor quis. Magnam nesciunt voluptatum pariatur repellat quibusdam iste voluptatibus praesentium nihil voluptates? Amet vero saepe earum!',
                currentPrice: '5 990 ₽',
                oldPrice: '5 990 ₽'
            }
        ]
    }
  },
}
</script>

<style scoped lang="scss">
@import "../styles/variables";

.main__productsList {
    display: grid;
    gap: 12px 16px;
    grid-template-columns: repeat(4, 1fr);
}

@media (max-width: $layout-breakpoint-large) {
  .main__productsList {
    grid-template-columns: repeat(3, 1fr);
  }
}
@media (max-width: $layout-breakpoint-medium) {
  .main__productsList {
    grid-template-columns: repeat(2, 1fr);
  }
}

</style>
  