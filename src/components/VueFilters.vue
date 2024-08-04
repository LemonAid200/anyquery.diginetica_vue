<template>
            <div class="main__filters">
                <div class="main__filters-categories">
                    <ul>
                        <li><span>Название категории</span> <span class="main__filters-categories__count">3</span></li>
                        <li><span>Название категории</span> <span class="main__filters-categories__count">3</span></li>
                        <li><span>Название категории</span> <span class="main__filters-categories__count">3</span></li>
                        <li><span>Название категории</span> <span class="main__filters-categories__count">3</span></li>
                    </ul>
                </div>
                <div class="main__filters-price">
                    <h3>Цена</h3>

                    <div class="main__filters-price__search">
                        <div class="main__filters-price__search__custom-input">
                            <span>от</span>
                            <input type="text" placeholder="5000">
                        </div>
                        <div class="main__filters-price__search__horizontal-line"></div>
                        <div class="main__filters-price__search__custom-input">
                            <span>от</span>
                            <input type="text" placeholder="5000">
                        </div>
                    </div>

                </div>
                <div class="main__filters-brands">
                    <div class="main__filters-brands__title-btn-wrapper">
                        <h3>Бренд</h3>
                        <button class="main__filters-brands-clearBtn">Очистить</button>
                    </div>

                    <div class="main__filters-brands__search">
                        <img src="../assets/images/search_light.svg" alt="">
                        <input type="text" placeholder="Поиск">
                    </div>
                    <div class="main__filters-brands-brandsList">
                        <ul>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="main__filters-size">
                    <h3>Размер</h3>
                    <div class="main__filters-size-sizeList">
                        <ul>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            <li>
                                <input type="checkbox" name="" id="">
                                <label>Атрибут</label>
                                <span>3</span>
                            </li>
                            
                        </ul>
                    </div>
                </div>
            </div>
</template>

<script>
export default {
  name: 'VueFilters',
  props: {
  }
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

  &-categories {
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
              cursor: pointer;

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

  &-price {
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

  &-brands {
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
          
          @include custom-border();

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

  &-size {
      margin-top: 28px;
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

</style>
