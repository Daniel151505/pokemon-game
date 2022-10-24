<template>
    <div class="options-container">
        <div>
            <li 
                v-for="pokemon in pokemons" 
                :key="pokemon.id"
                @click="$emit( 'selection', pokemon.id )">
                {{ pokemon.name }}
            </li>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        pokemons: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped>
    li {
        list-style-type: none;
        background-color: white;
        border-radius: 5px;
        border: 1px solid rgba(0, 0, 0, 0.2);
        cursor: pointer;
        margin-bottom: 10px;
        width: 250px;
    }

    li:hover {
        background-color: rgba(0, 0, 0, 0.05);
    }

    .options-container {
        display: flex;
        justify-content: center;
    }
</style>