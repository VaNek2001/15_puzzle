<script setup>
    import { ref } from "vue";
    const radio1 = [
        {
            input: {
                id: 'radio-1',
                value: '1',
            },
            label: {
                for: 'radio-1',
                title: '2x2'
            }
        },
        {
            input: {
                id: 'radio-2',
                value: '2',
            },
            label: {
                for: 'radio-2',
                title: '3x3'
            }
        },
        {
            input: {
                id: 'radio-3',
                value: '3',
                checked: 'true',
            },
            label: {
                for: 'radio-3',
                title: '4x4'
            }
        },
        {
            input: {
                id: 'radio-4',
                value: '4',
            },
            label: {
                for: 'radio-4',
                title: '5x5'
            }
        },
        {
            input: {
                id: 'radio-5',
                value: '5',
            },
            label: {
                for: 'radio-5',
                title: '6x6'
            }
        },
        {
            input: {
                id: 'radio-6',
                value: '6',
            },
            label: {
                for: 'radio-6',
                title: '7x7'
            }
        }
    ];
    const radio2 = [
        {
            input: {
                id: 'radio-7',
                value: '7',
            },
            label: {
                for: 'radio-7',
                title: '8x8'
            }
        },
        {
            input: {
                id: 'radio-8',
                value: '8',
            },
            label: {
                for: 'radio-8',
                title: '9x9'
            }
        },
        {
            input: {
                id: 'radio-9',
                value: '9',
            },
            label: {
                for: 'radio-9',
                title: '10x10'
            }
        },
    ]
    const picked = ref('3')
</script>

<template>
    <section class="game" id="game">
                <h1 class="my-6">ИГРА</h1>
                <div class="container1-lvl">
                    <div class="container11-lvl">
                        <div class="btn-lvl" v-for="(item, index) in radio1" :key="index">
                            <input :id="item.input.id" type="radio" name="radio" :value="item.input.value" 
                            :checked="item.input.checked" v-model="picked">
                            <label :for="item.label.for">{{item.label.title}}</label>
                        </div>
                    </div> 
                </div>
                <div class="container2-lvl">
                    <div class="container22-lvl">
                        <div class="btn-lvl" 
                        v-for="(item, index) in radio2" 
                        :key="index">
                            <input 
                            :id="item.input.id" 
                            type="radio" name="radio" 
                            :value="item.input.value" 
                            :checked="item.input.checked" 
                            v-model="picked">
                            <label :for="item.label.for">{{item.label.title}}</label>
                        </div>
                    </div>
                </div>

                <!-- <span>Выбрано:{{ picked}}</span> -->

                <div class="container3-lvl">
                    <p class="text-lvl">Размер поля:</p>
                    <div class="dropdown">
                        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                         2x2
                        </button>
                        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                          <li><a class="dropdown-item" href="#">2x2</a></li>
                          <li><a class="dropdown-item" href="#">3x3</a></li>
                          <li><a class="dropdown-item" href="#">4x4</a></li>
                          <li><a class="dropdown-item" href="#">5x5</a></li>
                          <li><a class="dropdown-item" href="#">6x6</a></li>
                          <li><a class="dropdown-item" href="#">7x7</a></li>
                          <li><a class="dropdown-item" href="#">8x8</a></li>
                          <li><a class="dropdown-item" href="#">9x9</a></li>
                          <li><a class="dropdown-item" href="#">10x10</a></li>
                        </ul>
                    </div>
                </div>

                <button type="button" class="btn-StartGame" id="btn-StartGameMobile"><img src="/btn-StartGame.svg" alt="btn-startGame"></button>


                <img src="/field-2x2.svg" alt="Game" class="fieldGame" v-if="picked === '1'">
                <img src="/field-3x3.svg" alt="Game" class="fieldGame" v-else-if="picked === '2'">
                <img src="/field-4x4.svg" alt="Game" class="fieldGame" v-else-if="picked === '3'">
                <img src="/field-5x5.svg" alt="Game" class="fieldGame" v-else-if="picked === '4'">
                <img src="/field-6x6.svg" alt="Game" class="fieldGame" v-else-if="picked === '5'">
                <img src="/field-7x7.svg" alt="Game" class="fieldGame" v-else-if="picked === '6'">
                <img src="/field-8x8.svg" alt="Game" class="fieldGame" v-else-if="picked === '7'">
                <img src="/field-9x9.svg" alt="Game" class="fieldGame" v-else-if="picked === '8'">
                <img src="/field-10x10.svg" alt="Game" class="fieldGame" v-else-if="picked === '9'">
               
                <div class="gameStatistic row flex-wrap">
                    <div class="col-3"></div>
                    <div class="col-3 my-auto">
                        <button type="button" class="btn-StartGame" id="btn-StartGame"><img src="/btn-StartGame.svg" alt="btn-startGame"></button>
                    </div>
                    <div class="col-1"></div>
                    <div class="col-3"  id="cl3">
                        <div class="container-st">
                            <div class="text-step">
                                <p class="text-step-s">Ходов:</p>
                                <p class="text-step-x">Х</p>
                            </div>
                            <div class="text-timer">
                                <p class="text-timer-t">Время:</p>
                                <p class="text-timer-x">ЧЧ:ММ:СС</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
</template>

<style scoped>

</style>