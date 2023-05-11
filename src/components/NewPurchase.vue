<script lang="ts">
import { defineComponent } from 'vue';
import PurchaseItem from '@/components/PurchaseItem.vue'
import Consumers from '@/components/Consumers.vue'
import ConsumerModel from '@/models/ConsumerModel';
import ItemModel from '@/models/ItemModel';

export default defineComponent({
    components: {
        PurchaseItem,
        Consumers
    },
    data() {
        return {
            includeThisUser: true,
            party: [
                new ConsumerModel("Koka", false),
                new ConsumerModel("Dima", false),
                new ConsumerModel("Anton", false)
            ],
            bill: [
                new ItemModel("First", 200),
                new ItemModel("Second", 300)
            ]
        };
    },
    methods:
    {
        addNewItem(){
            this.bill.push(new ItemModel("", 0));
        }
    }

})
</script>

<template>
    <div class="card">
        <div class="card-header">
            <h2 class="text-center ">Add purchase</h2>
        </div>

        <div class="card-body">
            <div class="text-center fs-5  mb-2">Bill</div>

            <ul class="list-group">
                <PurchaseItem v-for="item, index in bill" :item="item"/>
                <li class="list-group-item">
                    <button type="button" @click="addNewItem" class="btn btn-success w-100">Add another item</button>
                </li>
            </ul>

            <Consumers :userList="party" v-model:includeMe="includeThisUser" />

            <button type="button" class="btn btn-success w-100 my-2">Submit</button>
        </div>
    </div>
    
</template>