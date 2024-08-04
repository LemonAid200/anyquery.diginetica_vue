<template>
    <header class="header">
          <div class="header__header-logo__catalogue-btn-wrapper">
              <div class="header__logo">
                  <img src="../assets/images/logo.svg" alt="">
                  <h3>Логотип</h3>
              </div>
              <button class="header__catalogue-btn">Каталог</button>
          </div>

          <img class="header__arrow" src="../assets/images/arrow.svg" alt="">
       
          <div class="header__search">
              <img class="header__search__lens" src="../assets/images/search.svg" alt="">
              <input type="text" v-model="search" placeholder="Поиск по 100 000 товаров ">
              <div class="header__search__mobile-buttons">
                <img @click="search = ''" src="../assets/images/cross_icon.svg" alt="">
                <button class="header__search__mobile-buttons__search-button">Найти</button>
              </div>
          </div>

          <nav class="header__navigation">
              <ul>
                  <li>Информация о компании</li>
                  <li>Контакты</li>
                  <li>Полезные ссылки</li>
              </ul>
          </nav>
      </header>
</template>

<script>
export default {
  name: 'VueHeader',
  data() {
    return {
        search: 'Запрос'
    }
  },
  props: {
  }
}
</script>

<style scoped lang="scss">
@import "../styles/variables";

.header {
    display: flex;
    gap: 24px;
    justify-content: space-around;
    height: 72px;
    align-items: center;

    font-family: "Inter", sans-serif;
    font-optical-sizing: auto;
    font-style: normal;

    &__header-logo__catalogue-btn-wrapper{
        display: flex;
        gap: 8px;
        align-items: center;
    }

    &__logo {
        padding: 0 24px;
        display: flex;
        gap: 9px;
        cursor: pointer;
    }
    &__catalogue-btn {
        @include custom-border(rgb(115, 175, 244), 8px);
        width: 104px;
        height: 48px;
        font-size: 14px;
        font-weight: 500;
    }
    &__arrow {
        display: none;
    }

    &__search {
        @include custom-border(rgb(115, 175, 244), 10px);
        display: flex;
        width: -webkit-fill-available;
        padding: 0 16px;
        &__lens {
            margin-right: 12px;
            cursor: pointer;
        }
        
        input {
            @include unset-default();
            height: 50px;
            width: 100%;
        }

        &__mobile-buttons {
            display: none;

            img {
                cursor: pointer;
            }
        }
    }
    &__navigation {
        ul {
            display: flex;
            align-items: center;   
            gap: 20px;
            
            li {
                width: auto;
                font-size: 14px;
                font-weight: 400;
                line-height: 17px;
                text-wrap: nowrap;
                cursor: pointer;
                margin: 0;
                padding: 0;
                
                &:hover {
                    color: rgb(115, 151, 245);
                }
            } 
            
            
        }
    }
}

@media (max-width: $layout-breakpoint-medium) {
    .header__navigation {
        display: none;
    }
}
@media (max-width: $layout-breakpoint-small) {
    .header__header-logo__catalogue-btn-wrapper {
        display: none;
    }
    .header {
        padding: 0 16px;

        &__arrow {
            display: block;
        }
    }
    .header__search {
        border: none;
        border-radius: 0;
        border-bottom: 1px solid rgb(213, 213, 213);
        padding: 0;


        input {
        }
        &__lens {
            display: none;
        }    


        &__mobile-buttons {
            display: flex;
            align-items: center;
            gap: 18px;

            img {
                width: 17px;
                height: 17px;
            }

            &__search-button {
                @include unset-default;
                @include custom-border(rgb(115, 151, 245), 5px);

                background: rgb(115, 151, 245);
                color: rgb(255, 255, 255);
                font-size: 16px;
                font-weight: 400;
                line-height: 14px;
                width: 75px;
                height: 38px;
            }

        }
    }


}

</style>
  