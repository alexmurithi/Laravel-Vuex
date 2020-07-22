<template>
 <div class="product-list1">
     <h2>Product List One</h2>

     <ul v-for="product in saleProducts" class="nav">
         <li class="nav-item">
            <span class="name">{{product.name}}</span>
         <span class="price badge badge-success">${{product.price}}</span>
         </li>
     </ul>

     <div>
         <button class="btn btn-primary" @click="reducePrice(3)">Reduce Price</button>
     </div>
  </div>


</template>

<script>
    import {mapGetters} from 'vuex';
    import {mapActions} from 'vuex'; 
export default {
   
   computed:{
       products(){
           //this accesses the state property in store.js and returns products state object//
           return this.$store.state.products
       },
    //    saleProducts(){
    //        //this accesses the getter property in store.js and returns an object of saleProducts//

           
    //        return this.$store.getters.saleProducts;
    //    }
    ...mapGetters([
        'saleProducts'
    ])

   },
   methods:{
    //    reducePrice:function(amount){
    //     //    this.$store.state.products.forEach(product =>{
    //     //      product.price-=1
    //     //    });

    //     // this.$store.commit('reducePrice',amount)
    //     this.$store.dispatch('reducePrice',amount)
    //    }

    ...mapActions([
        'reducePrice'
    ])
   }
}
</script>

<style>

</style>