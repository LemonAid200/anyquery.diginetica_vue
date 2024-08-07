<template>
    <div  :class="['main__filters', { 'main__filters-open': isOpenOnMobile }]">
        <div @click="$emit('toggleMobileMenu')" class="main__filters__close-btn">
            <img src="../assets/images/arrow.svg" alt="">
        </div>

        <CategoriesList/>

        <PriceFilter/>

        <BrandsFilter/>
        
        <SizesFilter/>


    </div>
</template>

<script>
import SizesFilter from './customUI/SizesFilter.vue'
import CategoriesList from './customUI/CategoriesList.vue';
import PriceFilter from './customUI/PriceFilter.vue';
import BrandsFilter from './customUI/BrandsFilter.vue';

export default {
  name: 'VueFilters',
  props: {
    isOpenOnMobile: {
        type: Boolean,
        default: () => false
    }
  },
  components: {
    CategoriesList,
    PriceFilter,
    BrandsFilter,
    SizesFilter
  },
  data() {
    return {

    }
  },
}
</script>

<style scoped lang="scss">
@import "../styles/variables";


.main__filters {
  h3 {
    color: rgb(51, 51, 51);
    font-size: 16px;
    font-weight: 700;
    line-height: 20px;
  }

  &__close-btn {
    display: none;
    width: 100%;
    height: 20px;


    img {
        height: 12px;
    }
  }

  &-size {
      margin: 28px 0;
      
      &-sizeList {
          margin-top: 16px;

          ul {
              max-height: 290px;

              li {
                margin-top: 12px;
                padding-right: 16px;
                width: 273px;
                height: 20px;
                box-sizing: border-box;
                

                color: rgb(51, 51, 51);
                font-size: 14px;
                font-weight: 400;
                line-height: 16px;

                input {
                  height: 20px;
                  width: 20px;
                  box-sizing: border-box;
                  border: 1px solid rgb(213, 213, 213);
                  border-radius: 3px;
                  margin: 0;
                  float: left;

                }

                label {
                  height: 20px;
                  line-height: 20px;
                  float: left;
                  margin-left: 8px;
                }

                span {
                    float: right;
                    font-size: 12px;
                    font-weight: 400;
                    color: rgb(170, 170, 170);
                }
                &:first-child {
                    margin-top: 0;                                    
                }
              }
          }
      }
  }
}

@media (max-width: $layout-breakpoint-small) {
  .main__filters {
        @include custom-scroll;
        max-height: 100vh;
        overflow-y: scroll;
        overflow-x: visible;
        padding: 0 6px;
        position: fixed;
        background-color: white;
        top: 0;
        left: 0;
        z-index: 1000;
        opacity: 0;
        transition: transform ease-in-out 750ms;
        transform: translate(-100%, 0);

        &__close-btn {
            background: rgb(115,152,245);
            background: linear-gradient(90deg, rgba(115,152,245,0) 0%, rgba(115,152,245,0.30575980392156865) 50%, rgba(115,152,245,0) 100%);
            display: flex;
            justify-content: space-around;
            align-items: center;

            img {
                height: 12px;
            }
        }
    }

    .main__filters-open {
        opacity: 1;
        transition: transform ease-in-out 750ms;
        transform: translate(0, 0);
    }
}
</style>
