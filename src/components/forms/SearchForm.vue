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
input {
    background-color: transparent;
    border: 1px solid #182028;
    border-left: 0;
    border-right: 0;
    color: #2CA6A4;

    &:focus {
        outline: 0;
    }
}

button {
    background-color: #2CA6A4;
}
</style>