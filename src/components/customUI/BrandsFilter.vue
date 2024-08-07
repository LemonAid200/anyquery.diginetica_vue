<template>
    <div class="main__filters-brands">
            <div class="main__filters-brands__title-btn-wrapper">
                <h3>Бренд</h3>
                <button @click="brandSearch = ''" class="main__filters-brands-clearBtn">Очистить</button>
            </div>

            <div class="main__filters-brands__search">
                <img src="../../assets/images/search_light.svg" alt="">
                <input v-model="brandSearch" type="text" placeholder="Поиск">
            </div>
            <div class="main__filters-brands-brandsList">
                <ul>
                    <VueFilterAtributeItem v-for="id in 9" :key="id"/>
                </ul>
            </div>
        </div>
</template>
   
<script>
import VueFilterAtributeItem from './FilterAtributeItem.vue';

export default {
    name: 'VueBrandsFilter',
    components: {
        VueFilterAtributeItem
    },
    data() {
        return {
            brandSearch: ''
        }
    },
    
}
</script>

<style lang="scss">
@import "../../styles/variables";

.main__filters-brands {
    margin-top: 28px;

    &__title-btn-wrapper{
        display: flex;
        justify-content: space-between;
        height: 20px;

        h3 {
            text-align: left;
            margin-top: 0;
        }
        button {
            @include unset-default();
            color: rgb(170, 170, 170);
            font-size: 12px;
            font-weight: 400;
            line-height: 12px;
            text-decoration-line: underline;
        }
    }

    &__search {
        @include custom-border();

        margin-top: 16px;
        width: 280px;
        height: 36px;
        display: flex;
        align-items: center;
        padding: 0 12px;

        img {
            width: 12px;
            height: 12px;
            
        }        

        input {
            @include unset-default();

            margin-left: 8px;
            width: 100%;
        }

    }

    &-brandsList {
        margin-top: 16px;

        ul {
            @include custom-scroll();

            max-height: 180px;
            overflow-y: scroll;
            overflow-x: visible;
        }
    }
}
</style>
   