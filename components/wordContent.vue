<template>

    <div class="word_container">
        <div class="f_word_row">
            <input autocomplete="off" type="text" id="fr_f_input" maxlength="1" @keydown="onKeyUp">
            <input autocomplete="off" type="text" id="fr_s_input" maxlength="1" @keydown="onKeyUp">
            <input autocomplete="off" type="text" id="fr_t_input" maxlength="1" @keydown="onKeyUp">
            <input autocomplete="off" type="text" id="fr_fo_input" maxlength="1" @keydown="onKeyUp">
            <input autocomplete="off" type="text" id="fr_fi_input" maxlength="1" @keydown="onKeyUp">
        </div>
    </div>

</template>

<script>

    export default {
        data() {
            return {
                word: {
                    fr_f_input: '',
                    fr_s_input: '',
                    fr_t_input: '',
                    fr_fo_input: '',
                    fr_fi_input: '',
                }
            }
        },
        mounted() {
        },
        methods: {
            // verify input value == max length
            onKeyUp(e) {
                let input = e.target;
                let maxLength = input.maxLength;
                let value = input.value;
                if (value.length == maxLength) {
                    let nextInput = input.nextElementSibling;
                    if (nextInput) {
                        nextInput.focus();
                    }
                }
                // if key is backspace
                if (e.keyCode == 8) {

                    if(e.target.value.length != 0) {
                        e.target.value = '';
                        e.target.focus();
                        return;
                    } else {
                        let prevInput = input.previousElementSibling;
                        if (prevInput) {
                            prevInput.focus();
                        }
                    }

 
                }
            }
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
