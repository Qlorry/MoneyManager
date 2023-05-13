<script lang="ts">
import { defineComponent } from 'vue';
import DeptPerson from '@/components/DeptPerson.vue'
import Chart from 'chart.js/auto';

export default defineComponent({
    data() {
        return {
            chartConfig: {
                type: 'pie',
                data: {
                    labels: [
                        'Red',
                        'Blue',
                        'Yellow'
                    ],
                    datasets: [{
                        label: 'My First Dataset',
                        data: [300, 50, 100],
                        backgroundColor: [
                            'rgb(255, 99, 132)',
                            'rgb(54, 162, 235)',
                            'rgb(255, 205, 86)'
                        ],
                        hoverOffset: 3
                    }]
                }
            }

        };
    },
    components: {
        DeptPerson
    },
    mounted() {
        new Chart(this.$refs.deptCanvas as HTMLCanvasElement, this.chartConfig);
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
                            <DeptPerson :id="'test1'" />
                            <DeptPerson :id="'test2'" />
                            <DeptPerson :id="'test3'" />
                        </div>
                    </div>
                </div>
                <div class="col-md-7 col-sm-12">
                    <div style="max-height: 400px;">
                        <canvas ref="deptCanvas"></canvas>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>