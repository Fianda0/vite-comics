<script>
export default {
    name: "ProductCard",
    props: ["prodotto"]
}
</script>

<template>
    <div class="col-2">
        <img :src="prodotto.thumb" alt="">
        <p>{{ prodotto.series }}</p>
    </div>
</template>

<style>
.productCard {
    width: 25%;
}
img{
    width: 100%;
    height: 50%;
    object-fit: cover;
    object-position: top;
}
</style>