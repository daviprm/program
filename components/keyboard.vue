<template>
    <div class="keyboard">

        <div class="keyboard_row">
            <div class="normal_key">
                Q
            </div>
            <div class="normal_key">
                W
            </div>
            <div class="normal_key">
                E
            </div>
            <div class="normal_key">
                R
            </div>
            <div class="normal_key">
                T
            </div>
            <div class="normal_key">
                Y
            </div>
            <div class="normal_key">
                U
            </div>
            <div class="normal_key">
                I
            </div>
            <div class="normal_key">
                O
            </div>
            <div class="normal_key">
                P
            </div>
        </div>

        <div class="keyboard_row">
            <div class="normal_key">
                A
            </div>
            <div class="normal_key">
                S
            </div>
            <div class="normal_key">
                D
            </div>
            <div class="normal_key">
                F
            </div>
            <div class="normal_key">
                G
            </div>
            <div class="normal_key">
                H
            </div>
            <div class="normal_key">
                J
            </div>
            <div class="normal_key">
                K
            </div>
            <div class="normal_key">
                L
            </div>
        </div>

        <div class="keyboard_row">
            <div class="normal_key">
                Z
            </div>
            <div class="normal_key">
                X
            </div>
            <div class="normal_key">
            C
            </div>
            <div class="normal_key">
                V
            </div>
            <div class="normal_key">
                B
            </div>
            <div class="normal_key">
                N
            </div>
            <div class="normal_key">
                M
            </div>
        </div>

        <div class="keyboard_row">
            <div class="normal_enter">
                ENTER
            </div>
            <div class="normal_backspace">
                <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-backspace" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
                    <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                    <path d="M20 6a1 1 0 0 1 1 1v10a1 1 0 0 1 -1 1h-11l-5 -5a1.5 1.5 0 0 1 0 -2l5 -5z" />
                    <path d="M12 10l4 4m0 -4l-4 4" />
                </svg>
            </div>
        </div>




    </div>
</template>

<style scoped>

    .keyboard {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        row-gap: 10px;
    }

    .keyboard .keyboard_row {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        column-gap: 10px;
    }

    .keyboard .keyboard_row .normal_key {
        width: 50px;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: var(--sec);
        border-radius: 5px;
        color: white;
        font-weight: 800;
        font-size: 25px;
        transition: .2s ease-in-out;
        cursor: pointer;
    }

    .keyboard .keyboard_row .normal_key:hover {
        background: #19191b;
    }

    .keyboard .keyboard_row .normal_enter {
        width: 290px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: var(--sec);
        border-radius: 5px;
        color: white;
        font-weight: 800;
        font-size: 23px;
        transition: .2s ease-in-out;
        cursor: pointer;
    }

    .keyboard .keyboard_row .normal_enter:hover {
        background: #19191b;
    }

    .keyboard .keyboard_row .normal_backspace {
        width: 110px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        background: var(--sec);
        border-radius: 5px;
        font-weight: 800;
        font-size: 25px;
        transition: .2s ease-in-out;
        cursor: pointer;
    }

    .keyboard .keyboard_row .normal_backspace svg {
        width: 36px;
        height: 36px;
        stroke: white;
    }

    .keyboard .keyboard_row .normal_backspace:hover {
        background: #19191b;
    }

</style>