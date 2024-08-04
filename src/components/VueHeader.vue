<template>
    <header class="header">
          <div class="header__header-logo__catalogue-btn-wrapper">
              <div class="header__logo">
                  <img src="../assets/images/logo.svg" alt="">
                  <h3>Логотип</h3>
              </div>
              <button class="header__catalogue-btn">Каталог</button>
          </div>
          
          <div class="header__search">
              <img src="../assets/images/search.svg" alt="">
              <input type="text" placeholder="Поиск по 100 000 товаров ">
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
    &__search {
        @include custom-border(rgb(115, 175, 244), 10px);
        display: flex;
        width: -webkit-fill-available;
        padding: 0 16px;
        img {
            margin-right: 12px;
        }
        input {
            @include unset-default();
            height: 50px;
            width: 100%;
        }
    }
    &__navigation {
        ul {
            display: flex;    
            gap: 20px;
            
            li {
                font-size: 14px;
                font-weight: 400;
                line-height: 17px;
                text-wrap: nowrap;
                cursor: pointer;
            }            
        }
    }
}
</style>
  