<template>
    <div>
        <div>
            <b-breadcrumb :items="items"></b-breadcrumb>
        </div>
        <form>
            <p>Agregar Vehiculo</p>
            <p>Marca: <input type="text" required v-model="itemBrand"></p>
            <p>Modelo: <input type="text" required v-model="itemModel"></p>
            <p>Año de fabricacion: <input type="number" required v-model="itemYear"></p>

            <button type="submit">Add item</button>
          </form>
    </div>
</template>

<script>
export default {
    name: 'ExamenU1Form',

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
        ],

            errors: [],
            itemBrand: null,
            itemModel: null,
            itemYear: null,
            carList: [
                {item: this.item}
            ]
        };
    },

    mounted() {
        
    },

    methods: {
        addItem(){
            let item ={
                brand: this.itemBrand,
                model: this.itemModel,
                year: this.itemYear
            }
        this.carList.push(item)
        this.itemName = null
        this.itemNumber = null
        this.itemImportant = false
        }
    },
};
</script>

<style lang="scss" scoped>

</style>