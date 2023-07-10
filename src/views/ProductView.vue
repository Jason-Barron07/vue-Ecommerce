<template>
    <div class="container">
        <div class="row justify-content-center m-4 gap-3">
            <div class="card" v-for="product in products" style="width: 18rem;" :key="product.id">
                <img :src="product.image" class="card-img-top" :alt="products.make">
                <div class="card-body">
                  <h5 class="card-title">{{product.name}}</h5>
                  <p class="card-text">{{product.price}}</p>
                  <a href="/Items" class="btn btn-primary">Read more</a>
                </div>
              </div>
        </div>

    </div>
</template>

<script>
    export default {
        computed:{
            products(){
                return this.$store.state.products
            }
        },
        mounted(){
            this.$store.dispatch('fetchProducts')
        }
    }
</script>

<style scoped>



</style>