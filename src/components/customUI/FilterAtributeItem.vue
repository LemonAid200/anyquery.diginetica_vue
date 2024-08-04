<template>
    <li>
        <VueCustomCheckbox style="float: left;"/>
        <label>{{ atributeName }}</label>
        <span>3</span>
    </li>
</template>

<script>  
import VueCustomCheckbox from './CustomCheckbox.vue' 

export default {
name: 'VueFilterAtributeItem',
components:{
    VueCustomCheckbox
},
props: {
    atributeName: {
        type: String,
        default: () => 'Атрибут'
    }
}
}
</script>

<style lang="scss">
@import "../../styles/variables";
  
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


    label {
    height: 20px;
    line-height: 20px;
    float: left;
    margin-left: 12px;
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


</style>
  