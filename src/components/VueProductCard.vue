<template>
    <div class="main__productsList__productCard">
        <div class="main__productsList__productCard-image">
            <img class="main__productsList__productCard-image__picture" 
                :src="product.isInStock ? 
                require('@/assets/images/item_icon.svg') :
                require('@/assets/images/item_notInStock_icon.svg')" 
                alt="Product image" 
            >

            <div class="main__productsList__productCard-image__mark" v-if="product.isBestSeller">
                <span>Хит продаж</span>
                <img src="../assets/images/fire_icon.svg" alt="">
            </div>
            
            <div class="main__productsList__productCard-image__discountMark">
                <span>{{ product.discount }}</span>                            
            </div>
        </div>
        <span class="main__productsList__productCard-brand">{{ product.brand }}</span>
        <p class="main__productsList__productCard-name">{{ productName }}</p>
        <div class="main__productsList__productCard-price">
            <h2 class="main__productsList__productCard-currentPrice">{{ product.currentPrice }}</h2>
            <h3 class="main__productsList__productCard-oldPrice">{{ product.oldPrice }}</h3>      
        </div>
        <button v-if="product.isInStock" class="main__productsList__productCard-buyBtn">Купить</button>
        <button v-else class="main__productsList__productCard-remindWhenAvailable">Сообщить о поступлении</button>
    </div>       
</template>

<script>
export default {
    name: 'VueProductCard',
    props: {
        product: Object
    },
    computed: {
        productName(){
            return this.product.name.substring(0, 67) + '...'
        }
    },
}
</script>
    
<style scoped lang="scss">
@import "../styles/variables";



.main__productsList__productCard {
    height: 360px;
    text-align: left;
    
    &:hover &-image__picture  {
        transform: scale(calc(80/60));
        transition: transform ease 300ms;
    }

    &:hover &-name {
        color: rgb(18, 91, 174);
    }

    &-image {
        height: 200px;
        position: relative;
        background: rgb(248, 248, 250);
        display: flex;
        align-items: center;

        &__picture {
            display: block;
            margin: 0 auto;
            transition: transform ease 300ms;
        }

        &__mark {      
            position: absolute;
            height: 32px;
            width: 112px;
            top: 12px;
            left: 12px;      
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

        color: rgb(51, 51, 51);
        font-size: 14px;
        font-weight: 400;
        line-height: 16px;    
        margin-top: 8px;    
        height: 48px; 
        cursor: pointer;  
        text-align: left;
        overflow: hidden;
        display: -webkit-box;
        -webkit-line-clamp: 3;
        -webkit-box-orient: vertical;
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

    &-remindWhenAvailable {
        @include custom-border(rgb(170, 170, 170), 4px);
        @include hover-smart(white, rgb(170, 170, 170));

        box-sizing: border-box;
        width: 100%;
        height: 38px;
        color: rgb(170, 170, 170);
        font-size: 14px;
        font-weight: 700;
        line-height: 14px;  
        margin-top: 12px;
    }
}

@media (min-width: $layout-breakpoint-small) {
    .main__productsList__productCard {
        height: 372px;
    }
}
</style>
      