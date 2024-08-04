<template>
   <div class="main__filters-categories">
        <ul>
            <li v-for="(category, id) in Categories" :key="id">
                <span>{{ category.categoryName }}</span>
                <span class="main__filters-categories__count">
                    {{ category.count }}                    
                </span>
            </li>
        </ul>
    </div>
</template>
  
  <script>
 
  export default {
    name: 'VueCategoriesList',
    props: {
        Categories: {
            type: Array,
            default: () => [
                { categoryName: 'Название категории', count: 3 },
                { categoryName: 'Название категории', count: 3 },
                { categoryName: 'Название категории', count: 3 },
                { categoryName: 'Название категории', count: 3 },
            ]
        }

    }
    
  }
  </script>
  
<style lang="scss">
@import "../../styles/variables";

.main__filters-categories {
    ul {
        li {
            @include hover-smart( none, rgb(226, 239, 255));
            
            width: 280px;
            height: 30px;
            border-radius: 5px;
            box-sizing: border-box;
            padding-left: 32px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding-right: 16px;
            margin-top: 0;
            cursor: pointer;

            span {
                color: rgb(51, 51, 51);
                font-size: 14px;
                font-weight: 400;
                line-height: 16px;
            }

            .main__filters-categories__count {
                color: rgb(170, 170, 170);
                font-size: 12px;
                font-weight: 400;
                line-height: 14px;
            }

            &:first-child {
                padding-left: 8px;
            }
        }        
    }    
}
</style>
  