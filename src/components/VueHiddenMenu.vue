<template>
    <div :class="{ isOpen: hidden-menu-open }">
        <slot></slot>
    </div>
</template>

<script>  

export default {
name: 'VueHiddenMenu',
data() {
    return {
        isOpen: false,
    }
},
}
</script>

<style lang="scss">
// @import "../../styles/variables";

.hidden-menu-open {
    position: static;
    top: 0;
    left: 0;
    transform: translate(-100%, 0)
}


</style>
  