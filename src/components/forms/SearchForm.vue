<script>
export default {
    name: 'SearchForm',
    data() {
        return {

        }
    }
};
</script>
<template>
    <div class="d-flex">
        <input class="py-2" type="text" placeholder="Search..">
        <button class="text-white border-0 px-3">Search</button>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

input {
    background-color: transparent;
    border: 1px solid $light-blue;
    border-left: 0;
    border-right: 0;
    color: $primary;

    &:focus {
        outline: 0;
    }
}

button {
    background-color: $primary;
}
</style>