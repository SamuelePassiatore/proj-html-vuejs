<script>
export default {
    name: 'SendForm',

}
</script>

<template>
    <div class="send-form pb-5">
        <div class="container position-relative">
            <img src="../../assets/img/-m.png" alt="form-background" class="w-100">
            <div class="inputs d-flex justify-content-center">
                <input type="text" placeholder="First Name">
                <input type="text" placeholder="Last Name">
                <input type="email" placeholder="Email Address">
            </div>
            <button class="fw-bold">Subscribe</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.send-form {
    background-color: $dark-blue;

    .inputs {
        width: 100%;
        position: absolute;
        bottom: 55%;

        input {
            height: 50px;
            margin: 0 15px;
            padding: 15px 25px;
            border-radius: 30px;
            border: 1px solid $white;
            color: $white;
            background-color: transparent;

            &:focus {
                outline: 0;
            }

            &::placeholder {
                color: $white;
            }
        }
    }

    button {
        position: absolute;
        height: 50px;
        bottom: 30%;
        left: 50%;
        transform: translate(-50%);
        padding: 12px 40px;
        border-radius: 30px;
        color: $white;
        border: 0;
        background-color: $dark-blue;

        &:hover {
            background-color: $white;
            color: $dark-blue;
        }
    }

}
</style>