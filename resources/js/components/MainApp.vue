<template>
    <div class="container">
        <ProductListOne/>
        <ProductListTwo/>
    </div>
</template>

<script>
   import ProductListOne from './ProductListOne';
   import ProductListTwo from './ProductListTwo';

   import {store} from '../store/store';

    export default {
        store:store,

        mounted() {
            console.log('Component mounted.')
        },
        
        components:{
          ProductListOne,
          ProductListTwo,
        },
        
    }
</script>
