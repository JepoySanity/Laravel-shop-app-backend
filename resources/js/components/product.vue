<template>
    <div class="card" style="width: 18rem">
        <img
            src="https://store.storeimages.cdn-apple.com/8756/as-images.apple.com/is/macbook-air-space-gray-select-201810?wid=446&hei=410&fmt=jpeg&qlt=95&.v=1633027804000"
            class="card-img-top"
            alt="..."
        />
        <div class="card-body">
            <h5 class="card-title">{{ product.product_name }}</h5>
            <p class="card-text">
                {{ product.product_details }}
            </p>
            <a href="#" class="btn btn-primary">Add to cart</a>
        </div>
    </div>
</template>
<script>
export default {
    props: ["product"],
};
</script>
<style>
.card-text {
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2; /* number of lines to show */
    line-clamp: 2;
    -webkit-box-orient: vertical;
}
</style>
