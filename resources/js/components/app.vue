<template lang="">
    <div>
        <navbar></navbar>
        <products :products="products" />
    </div>
</template>
<script>
import axios from "axios";
import navbar from "./layout/navbar";
import products from "./products";
export default {
    data: function () {
        return {
            products: [],
        };
    },
    components: {
        navbar,
        products,
    },
    methods: {
        getProducts() {
            axios
                .get("api/products")
                .then((response) => {
                    this.products = response.data;
                })
                .catch((error) => {
                    console.log(error);
                });
        },
    },
    created() {
        this.getProducts();
    },
};
</script>
