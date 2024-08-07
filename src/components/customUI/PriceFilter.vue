<template>
    <div class="main__filters-price">
        <h3>Цена</h3>
        <div class="main__filters-price__search">
            <div class="main__filters-price__search__custom-input">
                <span>от</span>
                <input type="text" v-model="minPrice" @focusout="minPrice = formatCurrency(minPrice)" placeholder="5 500 ₽">
            </div>
            <div class="main__filters-price__search__horizontal-line"></div>
            <div class="main__filters-price__search__custom-input">
                <span>до</span>
                <input type="text" v-model="maxPrice" @focusout="maxPrice = formatCurrency(maxPrice)" placeholder="5 500 ₽">
            </div>
        </div>
    </div>
</template>
   
   <script>
  
    export default {
        name: 'PriceFilter',
        data() {
            return {
                minPrice: '',
                maxPrice: '',
            }
        },
        methods: {
            formatCurrency(value){
                const formattedValue = value.toString().replace(/[^0-9]/g, '').replace(/\B(?=(\d{3})+(?!\d))/g, ' ');
                if (formattedValue === '') return ''
                return formattedValue + ' ₽';
            }
        }
    }
   </script>
   
<style lang="scss">
@import "../../styles/variables";

.main__filters-price {
    margin-top: 28px;
    &__search {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;

        &__custom-input {
            @include custom-border();
            display: flex;
            align-items: center;
            width: 119px;
            height: 36px;

            span {
                display: inline-block;
                line-height: 36px; 
                height: 38px;
                font-size: 12px;
                font-weight: 400;
                color: rgb(170, 170, 170);
                margin-left: 8px;
            }
            input {
                @include unset-default();
                width: 100%;
                margin-left: 6px;
                color: rgb(51, 51, 51);
                font-family: PT Sans;
                font-size: 14px;
                font-weight: 400;
                line-height: 16px;

                &::placeholder {
                    color: rgb(51, 51, 51);
                    font-family: PT Sans;
                    font-size: 14px;
                    font-weight: 400;
                    line-height: 16px;
                }
            }
        }

        &__horizontal-line{
            width: 10px;
            height: 1px;
            background: rgb(213, 213, 213);
        }

    }

}

</style>
   