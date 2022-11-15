<script>
import { store } from '../assets/js/store';
import Actor from "./Actor.vue";
export default {
    name: `ListActors`,
    components: {
        Actor
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
            <Actor v-for="item in store.characters" :item="item"></Actor>
        </div>
    </section>

</template>

<style>

</style>