<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({
    props: {
        id: String,
        accordionParent: String
    },
    data() {
        return {
        };
    },
    computed:
    {
        targetId() { return `#${this.id}`; },
        targetAccordionParent() { return `#${this.accordionParent}`; }
    }
})
</script>

<template>
    <div class="accordion-item">
        <h2 class="accordion-header">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" :data-bs-target="targetId"
                aria-expanded="false" :aria-controls="id">
                <div class="d-flex flex-column">
                    <div class="fs-5">To Dima</div>
                    <div class="d-flex gap-2 mt-1">

                        <div class="p-2 border border-secondary rounded">Raw: 100000</div>
                        <div class="p-2 border border-secondary rounded">Total: 1000</div>
                    </div>
                </div>

            </button>
        </h2>
        <div :id="id" class="accordion-collapse collapse" :data-bs-parent="targetAccordionParent">
            <div class="accordion-body">
                <ul class="list-group">
                    <li class="list-group-item d-flex justify-content-between align-items-center">
                        A list item
                        <span class="badge bg-primary rounded-pill">14</span>
                    </li>
                    <li class="list-group-item d-flex justify-content-between align-items-center">
                        A second list item
                        <span class="badge bg-primary rounded-pill">2</span>
                    </li>
                    <li class="list-group-item d-flex justify-content-between align-items-center">
                        A third list item
                        <span class="badge bg-primary rounded-pill">1</span>
                    </li>
                </ul>

                <div class="d-flex flex-row align-items-center ps-2 pt-2">
                    <div class="me-2"> Pay: </div><input class="form-control flex-grow" type="text" placeholder="Amount"
                        aria-label="Purchase name">
                </div>
                <button type="button" class="btn btn-success w-100 my-2">Submit</button>
            </div>
        </div>
    </div>
</template>