<template>

    <div class="word_container">
            {{currentWord}}
        <div class="f_word_row">
            <div
                class="f_word_item"
                v-for="(item, index) in size"
                :class="{'actual' : index == currentInput}"
                :key="index"
                :value="currentWord[index]"
                :ref="'fr_' + index + '_input'"
            >{{currentWord[index]}}</div>
        </div>
    </div>

</template>

<script>
    const Mousetrap = require('mousetrap');

    export default {
        data() {
            return {
                size: 5,
                word: {},
                actualWord: 'casas',
                currentWord: [],
                actualfodase: 'asdasda',
                firstWord: [],
                secondWord: [],
                thirdWord: [],
                fourthWord: [],
                fivethWord: [],
                letters: ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'ç'],
            }
        },
        computed: {
            teste() {
                return Object.values(this.word).filter(Boolean);
            },
            currentInput() {
                return this.currentWord.length;
            }
        },
        mounted() {
            this.letters.forEach(element => {
                Mousetrap.bind(element, () => {
                    if(this.currentWord.length < this.size) {
                        this.currentWord.push(element);
                    }
                });
            });
            Mousetrap.bind('backspace', () => { 
                if(this.currentWord.length > 0) {
                    this.currentWord.pop();
                }
            });
            Mousetrap.bind('enter', () => { 
                // compare currentWord with actualWord
                if(this.currentWord.join('') == this.actualWord) {
                    alert('ACERTOUUUU')
                }
            });
        },
        methods: {
        }
    }

</script>


<style scoped>


    .actual {
        margin-top: -9px;
        transition: .3s;
    }

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

    .word_container .f_word_row .f_word_item {
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
