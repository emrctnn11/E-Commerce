<template>
    <div class="container" style="padding-top: 25px;">
        <div class="row">
            <div class="col-12 text-center">
                <h3 class="pt-3">Ürünler</h3>
                <router-link :to="{name: 'AddCategory'}">
                    <button class="btn btn-danger" style="float:right"> Ürün Ekle</button>
                </router-link>
            </div>
            <div>{{ categories }}</div>
        </div>
        <div class="row">
            <div v-for="category of categories" :key="category.id" class="col-12 pt-3 col-xl-4 col-md-6 d-flex">
                <CategoryBox :category="category"></CategoryBox>
            </div>
        </div>
    </div>
</template>

<script>
import CategoryBox from "../../components/Category/CategoryBox.vue";
const axios = require("axios");


export default {
    data() {
        return {
            // baseURL: "https://api.akilliticaretim.com",
            items: [
                {
                stockName: "Bulasik Makinasi",
                description: "Bulasiklarinizi yikayan makine",
                stockCode: "1",
                }
            ],
            categories: [],
        };
    },
    methods: {
        async getCategories() {
            await axios.get(`${this.baseURL}/api/Product/ListProducts`)
                .then(res => this.categories = res.data)
                .catch(err => console.log(err));
        }
    },
    mounted() {
        this.getCategories();
    },
    components: { CategoryBox }
};
</script>

<style scoped>

</style>