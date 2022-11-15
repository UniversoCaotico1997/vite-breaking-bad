<script>
import { store } from '../assets/js/store';
import Actors from "./Actor.vue";
export default {
    name: `ListActors`,
    components: {
        Actors
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>

    <section class="list_actors">
        <div class="row row-cols-5">
            <Actors v-for="item in store.characters" :item="item"></Actors>
        </div>
    </section>

</template>

<style>

</style>