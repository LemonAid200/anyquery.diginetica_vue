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
    name: 'CustomCheckbox',

    data() {
        return {
            isChecked: false,
        };
    },
    computed: {
        checkboxId() {
            return Math.random().toString(36).substring(2, 9);
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

    .custom-checkbox {
        display: inline-block;
        cursor: pointer;
    }

    input[type="checkbox"] {
        display: none;
    }

    label {
        display: inline-block;
        width: 20px;
        height: 20px;
        background-image: url('../../assets/images/unchecked_icon.svg');
        background-size: cover;
    }

    .checked {
        background-image: url('../../assets/images/checked_icon.svg');
        width: 100%;
        height: 100%;
    }
</style>
