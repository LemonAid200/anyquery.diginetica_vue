<template>
<div class="custom-checkbox" @click="toggleCheckbox">
    <input type="checkbox" id="checkbox" v-model="isChecked" />
    <label :for="checkboxId">
    <span v-if="isChecked" class="checked"></span>
    <span v-else class="unchecked"></span>
    </label>
</div>
</template>

<script>
export default {
name: 'VueCustomCheckbox',

data() {
    return {
    isChecked: false,
    };
},
computed: {
    checkboxId() {
        return Math.random().toString(36).substr(2, 9);
    },
},
methods: {
    toggleCheckbox() {
        this.isChecked = !this.isChecked;
    },
},
};
</script>
  
<style scoped>
/* @import "../../styles/variables"; */

.custom-checkbox {
display: inline-block;
cursor: pointer;

}

input[type="checkbox"] {
display: none; /* Скрываем стандартный чекбокс */
}

label {
display: inline-block;
width: 20px; /* Ширина для изображения */
height: 20px; /* Высота для изображения */
background-image: url('../../assets/images/unchecked_icon.svg'); /* Изображение для невыбранного состояния */
background-size: cover;
}

.checked {
background-image: url('../../assets/images/checked_icon.svg'); /* Изображение для выбранного состояния */
width: 100%; /* Занимает всю ширину */
height: 100%; /* Занимает всю высоту */
}
</style>
