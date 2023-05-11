<script lang="ts">
import { defineComponent } from 'vue';
import DeptPerson from '@/components/DeptPerson.vue'

export default defineComponent({
    data() {
        return {};
    },
    components: {
        DeptPerson
    }
})
</script>

<template>
    <div class="card">
        <div class="card-header">
            <h2 class="">My Dept</h2>
        </div>

        <div class="card-body">
            <div class="row">
                <div class="col-md-5 col-sm-12">
                    <div class="overflow-auto" style="max-height: 400px;">
                        <div class="accordion" id="accordionExample">
                            <DeptPerson :id="'test1'"/>
                            <DeptPerson :id="'test2'"/>
                            <DeptPerson :id="'test3'"/>
                        </div>
                    </div>
                </div>
                <div class="col-md-7 col-sm-12">

                </div>
            </div>

        </div>
    </div>
</template>