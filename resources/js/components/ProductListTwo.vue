<template>
  <div class="product-list2">
     <h2>Product List Two</h2>

     <ul v-for="product in saleProducts" class="nav">
         <li class="nav-item">
            <span class="name">{{product.name}}</span>
         <span class="price">${{product.price}}</span>
         </li>
     </ul>
  </div>
  

  
</template>

<script>
import { mapGetters } from 'vuex'
export default {
    computed:{
        products(){
            return this.$store.state.products
        },
    //     saleProducts(){
    //        return this.$store.getters.saleProducts;
    //    }

    ...mapGetters([
        'saleProducts'
    ])
    }
}
</script>

<style>

</style>