<template>
<div>
    <Header></Header>
    <div class="white container padding" style="margin-top: 80px">
        <nuxt />
    </div>
    <div class="alert alert-info mt-4">
        <p align="center">
            Nous sommes à l'attente de toute proposition d'évolution de ce projet
            open-source.
        </p>
    </div>
</div>
</template>

<script>
import Header from "~/components/Header.vue";

export default {
    components: {
        Header,
    },
};
</script>

<style>
.gris {
    background-color: #fafafa;
}

.padding {
    padding: 10px 10px 10px 10px;
}

.white {
    background-color: white;
}
</style>
