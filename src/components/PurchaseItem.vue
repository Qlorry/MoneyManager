<script lang="ts">
import ItemModel from '@/models/ItemModel';
import { defineComponent } from 'vue';

export default defineComponent({
    props: {
        item: ItemModel
    },
    computed:
    {
        itemName(){
            return this.item ? this.item.name : "";
        },
        itemValue(){
            return this.item ? this.item.value : "";
        }
    },
    methods:
    {
        setItemName(event: any) {
            if(this.item)
                this.item.name = event.target.value;
        },
        setItemValue(event: any) {
            if(this.item)
                this.item.value = event.target.value;
        }
    }
})
</script>

<template>
    <li class="list-group-item">
        <input class="form-control mb-1" type="text" placeholder="Purchase name" aria-label="Purchase name"
        :value="itemName"
        @input="setItemName" >

        <div class="d-flex flex-row align-items-center ps-2">
            <div class="me-2"> Price: </div>
            <input class="form-control flex-grow" type="number" placeholder="Price" aria-label="Purchase name"
            :value="itemValue"
            @input="setItemValue" >

        </div>
    </li>
</template>