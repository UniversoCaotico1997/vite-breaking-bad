<script>
export default {
    name: `ListActors`,
}
</script>

<template>

    <section class="list_actors">
        <div class="row row-cols-5">
            <div class="col g-4 " v-for="item in store.characters">
                <div class="actor">
                    <div class="card p-3">
                        <img :src="item.img" class="card-img-top" alt="">
                        <div class="card-body text-center">
                            <h5 class="card-title">{{ item.name }} </h5>
                            <p class="card-text">{{ item.category }}</p>
                            <p class="card-text">{{ item.status }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>

<style>

</style>