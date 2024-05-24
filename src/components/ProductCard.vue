<script>
export default {
    name: "ProductCard",
    props: ["prodotto"]
}
</script>

<template>
    <div class="col-2">
        <img :src="element.thumb" alt="">
        <p>{{ element.series }}</p>
    </div>
</template>

<style>
.productCard {
    width: 25%;
}
</style>