<script lang="ts">
import { defineComponent } from 'vue';
import CreditItem from '@/components/CreditItem.vue'

export default defineComponent({
    components: {
        CreditItem
    },
    data() {
        return {};
    }
})
</script>

<template>
    <div class="card mt-3">
        <div class="card-header">
            <h2 class="">My Credits</h2>
        </div>

        <div class="card-body">
            <div class="row">
                <div class="col-5">
                    <div class="overflow-auto" style="max-height: 400px;">
                        <ul class="list-group">
                            <CreditItem />
                            <CreditItem />
                            <CreditItem />
                        </ul>
                    </div>
                </div>
                <div class="col-7">

                </div>
            </div>

        </div>
    </div>
</template>