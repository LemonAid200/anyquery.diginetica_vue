<template>
    <div class="main__filters-size">
        <h3>Размер</h3>
        <div class="main__filters-size-sizeList">
            <ul>
                <VueFilterAtributeItem v-for="id  in 6" :key="id * 100"/>            
            </ul>
        </div>
    </div>
</template>
   
<script>
import VueFilterAtributeItem from './FilterAtributeItem.vue';

export default {
    name: 'VueSizesFilter',
    components: {
        VueFilterAtributeItem
    },
    data() {
        return {
        }
    },
    
}
</script>

<style lang="scss">
@import "../../styles/variables";

.main__filters-size {
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
</style>
   