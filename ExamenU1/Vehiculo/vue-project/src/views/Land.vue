<template>
    <div>
        <b-breadcrumb :items="items"></b-breadcrumb>
    </div>
</template>

<script>
import FormVue from './Form.vue';
import Pagination from './Pagination.vue';

export default {
    name: 'ExamenU1Land',

    data() {
        return {
            items: [
          {
            text: 'Land',
            to:{name:Land}
          },
          {
            text: 'Paginatio',
            to:{name:Pagination}
          },
          {
            text: 'Form',
            to:{name:Form}         
         }
        ]
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>

</style>