<template>

    <div class="word_container">
        <div class="f_word_row">
            <input autocomplete="off" type="text" id="txt1" maxlength="1">
            <input autocomplete="off" type="text" id="txt2" maxlength="1">
            <input autocomplete="off" type="text" id="txt3" maxlength="1">
            <input autocomplete="off" type="text" id="txt4" maxlength="1">
            <input autocomplete="off" type="text" id="txt5" maxlength="1">
        </div>
        <div class="f_word_row">
            <input autocomplete="off" type="text" id="txt1" maxlength="1">
            <input autocomplete="off" type="text" id="txt2" maxlength="1">
            <input autocomplete="off" type="text" id="txt3" maxlength="1">
            <input autocomplete="off" type="text" id="txt4" maxlength="1">
            <input autocomplete="off" type="text" id="txt5" maxlength="1">
        </div>
        <div class="f_word_row">
            <input autocomplete="off" type="text" id="txt1" maxlength="1">
            <input autocomplete="off" type="text" id="txt2" maxlength="1">
            <input autocomplete="off" type="text" id="txt3" maxlength="1">
            <input autocomplete="off" type="text" id="txt4" maxlength="1">
            <input autocomplete="off" type="text" id="txt5" maxlength="1">
        </div>
        <div class="f_word_row">
            <input autocomplete="off" type="text" id="txt1" maxlength="1">
            <input autocomplete="off" type="text" id="txt2" maxlength="1">
            <input autocomplete="off" type="text" id="txt3" maxlength="1">
            <input autocomplete="off" type="text" id="txt4" maxlength="1">
            <input autocomplete="off" type="text" id="txt5" maxlength="1">
        </div>
        <div class="f_word_row">
            <input autocomplete="off" type="text" id="txt1" maxlength="1">
            <input autocomplete="off" type="text" id="txt2" maxlength="1">
            <input autocomplete="off" type="text" id="txt3" maxlength="1">
            <input autocomplete="off" type="text" id="txt4" maxlength="1">
            <input autocomplete="off" type="text" id="txt5" maxlength="1">
        </div>
    </div>

</template>

<script>

    export default {
        data() {
            return {
            }
        },
        mounted() {
        },
        methods: {

        }
    }

</script>


<style scoped>

    .word_container {
        display: flex;
        flex-direction: column;
        align-items: center;
        row-gap: 10px;
    }

    .word_container .f_word_row {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        column-gap: 10px;
    }

    .word_container .f_word_row input {
        width: 60px;
        height: 60px;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
        background: var(--sec);
        color: white;
        border-radius: 5px;
        font-weight: 800;
        font-size: 25px;
        cursor: pointer;
        outline: none;
        caret-color: transparent;
        text-transform: uppercase;
    }

    .word_container .f_word_row input:focus {
        margin-top: -6px;
    }


</style>