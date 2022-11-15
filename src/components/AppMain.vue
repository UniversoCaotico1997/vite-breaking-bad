<script>
import ListActors from "../components/ListActors.vue";
export default {
    name: `AppMain`,
    components: {
        ListActors
    },
}
</script>

<template>

    <main>
        <div class="filter container">
            <select class="">
                <option value="">Select category</option>
            </select>
        </div>


        <div class="container bg-white p-5">

            <div class="alert dark" role="alert">
                <strong>Found 62</strong> Characters
            </div>
            <ListActors></ListActors>

        </div>
    </main>
</template>

<style lang="scss" scoped>
@use"../assets/scss/variabels/variable" as *;

.card {
    height: 100%;
    background-color: $bb-primary;
    border: 0;
    border-radius: 0;


    img {
        height: 300px;
        object-fit: cover;
    }
}

.alert.dark {
    background-color: $bb-primary;
    color: white;
}

.filter {
    select {
        padding: .75rem;
        margin-bottom: 1rem;
        border-radius: 0.5rem;
    }
}
</style>