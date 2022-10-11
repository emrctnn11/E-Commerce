<template>
    <div class="card">
        <div class="embed-responsive embed-responsive-16by9">
            <img class="card-img-top" src="category.stockCode" alt="">
        </div>
        <div class="card-bod">
            <h5 class="card-title">
                {{category.stockName}}
            </h5>
            <p class="card-text">
                {{category.description}}
            </p>
            <a href="#" class="btn btn-danger">Go to buy</a>
        </div>
    </div>
</template>
<script>
export default {
    name: "CategoryBox",
    props: ["category"],
    methods: {
    },
};

</script>


<style scoped>
.card-img-top{
    object-fit: cover;
}

</style>