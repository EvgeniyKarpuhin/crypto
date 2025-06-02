<template>
  <input min="0" type="number" @input="changeAmount($event.target.value)" placeholder="Введите число"></br>
  <div>
    <button @click="convert()">Конверитровать</button>
    <button @click="favourite()" class="btn-mrg">В избранное</button>
  </div>
  
</template>

<script>
    export default {
        props: {
            changeAmount: {
                type: Function,
                required: true
            },
            convert: {
                type: Function,
                required: true
            },
            favourite: {
                type: Function,
                required: true
            }
        }
    }
</script>

<style scoped>
    input {
        outline: none;
        width: 500px;
        position: relative;
        top: -50px;
        font-size: 1.2em;
        border-radius: 3px;
        border: 0;
        padding: 10px;
        background: #fafafa;
        color: #333;
    }

    button {
        margin-bottom: 30px;
        padding: 15px 20px;
        text-transform: uppercase;
        color: #fff;
        cursor: pointer;
        background: #1a032d;
        border: 0;
        border-radius: 3px;
        transition: transform 500ms ease;
    }

    button:hover {
        transform: scale(1.1);
    }

    button.btn-mrg {
        margin-left: 20px;
    }
</style>