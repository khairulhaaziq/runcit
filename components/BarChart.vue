<template>
	<Bar id="my-chart-id" :options="chartOptions" :data="chartData" />
</template>

<script setup>
import { Bar } from "vue-chartjs";
import {
	Chart as ChartJS,
	Title,
	Tooltip,
	Legend,
	BarElement,
	CategoryScale,
	LinearScale,
} from "chart.js";

ChartJS.register(
	Title,
	Tooltip,
	Legend,
	BarElement,
	CategoryScale,
	LinearScale
);

const props = defineProps({
  chartData: {
    type: Object,
    required: true,
  }
});

const chartOptions = ref({
       aspectRatio: 3/2,
       scales: {x: {
        border: {
          display: false
        },
        grid: {
          display: false
        }
      },
      y: {
        border: {
          display:false
        },
       grid: {
              color: "#232323"
       }}},
	responsive: true,
	plugins: {
		legend: {
			display: false,
			labels: {
				// This more specific font property overrides the global property
				font: {
                                   family: "Inter",
					size: 14,
				},
			},
		},
	},
	interaction: { intersect: false },
});

</script>
