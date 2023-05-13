<script lang="ts">
import { defineComponent } from 'vue';
import CreditItem from '@/components/CreditItem.vue'
import Chart from 'chart.js/auto';

export default defineComponent({
    components: {
        CreditItem
    },
    data() {
        return {
            chartData: {
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
        };
    },
    mounted() {
        const chartConfig = {
                type: 'pie',
                data: this.chartData
            };
        new Chart(this.$refs.creditCanvas as HTMLCanvasElement, chartConfig);
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
                <div class="col-md-5 col-sm-12">
                    <div class="overflow-auto" style="max-height: 400px;">
                        <ul class="list-group">
                            <CreditItem />
                            <CreditItem />
                            <CreditItem />
                        </ul>
                    </div>
                </div>
                <div class="col-md-7 col-sm-12">
                    <div style="max-height: 400px;">
                        <canvas ref="creditCanvas"></canvas>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>