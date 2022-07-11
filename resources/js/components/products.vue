<template>
    <div class="container">
        <div class="row mt-4">
            <div
                v-for="(product, index) in products"
                :key="index"
                class="col-lg-3 mb-4"
            >
                <product :product="product" :key="index" />
            </div>
        </div>
    </div>
</template>
<script>
import product from "./product";
export default {
    props: ["products"],
    components: {
        product,
    },
};
</script>
