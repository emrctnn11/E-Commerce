<template>
    <div class="container" style="padding-top: 25px;">
        <div class="row">
            <div class="text-center col-12">
                <h3>
                Ürün Ekleyin.
                </h3>
                <router-link :to="{name: 'Category'}">
                    <button class="btn btn-danger" style="float:right">Ürünleri Göster</button>
                </router-link>
            </div>
        </div>
        <div class="row">
            <div class="col-3"></div>
            <div class="col-6">
                <form>
                    <div class="form-group">
                        <label>Ürün Adı</label>
                        <input type="text" class="form-control" v-model="stockName">
                    </div>
                    <div class="form-group">
                        <label>Ürünün Detayları</label>
                        <input type="text" class="form-control" v-model="description">
                    </div>
                    <div class="form-group">
                        <label>Fotoğrafı</label>
                        <input type="text" class="form-control" v-model="stockCode">
                    </div>
                    <button type="button" class="btn btn-danger" @click="addCategory">Submit</button>
                </form>
            </div>
            <div class="col-3"></div>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
import sweetalert from 'sweetalert'

export default {

    data() {
        return {
            stockName: "",
            description: "",
            stockCode: "",
        };
    },

    methods: {
        addCategory(){
            console.log(this.stockName, this.description);
            const newCategory = {
                stockName: this.stockName,
                description: this.description,
                stockCode: this.stockCode,
            };

            const baseURL ="https://api.akilliticaretim.com"

            axios({
                method: "post",
                url: `${baseURL}/api/Product/SaveProduct`,
                data: JSON.stringify(newCategory),
                headers: {
                    "Content-Type": "application/json"
                }
            })
            
            .then(()=> {
                sweetalert({
                    text: 'Category added Successfully',
                    icon: 'Success',
                });
            })
            .catch(err => {
                console.log(err);
            })
        },
    },
};
</script>

<style scoped>

</style>