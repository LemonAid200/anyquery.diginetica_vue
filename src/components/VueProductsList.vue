<template>
<div class="main__productsList">
    <VueProductItem v-for="product in productsList" :product="product" :key="product.id"/>    
</div>
</template>

<script>
import VueProductItem from './VueProductItem.vue'

export default {
  name: 'VueProductsList',
  components: {
    VueProductItem
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
                oldPrice: '5 990 ₽'
            },
            {
                brand: 'Бренд',
                discount: '12%',
                isBestSeller: true,
                isInStock: true,
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

                &__productCard {
                    height: 360px;
                    
                    &-image {
                        height: 200px;
                        position: relative;
                        background: rgb(248, 248, 250);
                        align-content: center;

                        &__picture {
                            display: block;
                            margin: 0 auto;
                        }

                        &__mark {      
                            position: absolute;
                            height: 32px;
                            width: 112px;
                            top: 12px;
                            left: 2px;      
                            box-sizing: border-box;
                            border: 1px solid rgb(242, 242, 242);
                            border-radius: 4px;
                            background: rgb(255, 255, 255);
                            display: flex;
                            align-items: center;
                            justify-content: space-between;
                            padding: 0 8px;
                        }
                        &__discountMark {  
                            position: absolute;
                            width: 48px;
                            height: 24px;
                            left: 12px;
                            bottom: 12px;    
                            border-radius: 4px;
                            background: rgb(115, 151, 245);
                            display: flex;
                            align-items: center;
                            justify-content: center;
                            color: rgb(255, 255, 255);
                            font-size: 14px;
                            font-weight: 700;
                            line-height: 14px;
                        }
                    }

                    &-brand {               
                        color: rgb(170, 170, 170);
                        font-size: 14px;
                        font-weight: 400;
                        line-height: 16px;
                        display: block;
                        margin-top: 12px;
                    }
                    &-name {     
                        @include hover-smart(rgb(18, 91, 174), none);
                        color: rgb(51, 51, 51);
                        font-size: 14px;
                        font-weight: 400;
                        line-height: 16px;    
                        margin-top: 8px;    
                        height: 48px; 
                        cursor: pointer;  
                    }
                    &-price {    
                        display: flex;  
                        gap: 8px;
                        align-items: center;  
                        margin-top: 12px;
                        height: 14px;           
                    }
                    &-currentPrice {   
                        color: rgb(51, 51, 51);
                        font-size: 16px;
                        font-weight: 700;
                        line-height: 14px;            

                    }
                    &-oldPrice {   
                        color: rgb(170, 170, 170);
                        font-size: 12px;
                        font-weight: 400;
                        line-height: 14px;
                        text-decoration-line: line-through; 

                    }
                    &-buyBtn {
                        @include custom-border(rgb(115, 175, 244), 4px);
                        @include hover-smart(white, rgb(115, 151, 245));

                        box-sizing: border-box;
                        width: 75px;
                        height: 38px;
                        color: rgb(115, 151, 245);
                        font-size: 14px;
                        font-weight: 700;
                        line-height: 14px;  
                        margin-top: 12px;
                    }
                }

            }
</style>
  