<template>
	<div class="grid grid-cols-3 gap-5">
	<!--
		<div
			class="col-span-1 rounded-lg bg-[#161616] border border-[#232323] p-5"
		>
			<BarChart :chartData="chartData" />
		</div>
		<div
			class="col-span-1 rounded-lg bg-[#161616] border border-[#232323] p-5"
		>
			<LineChart :chartData="lineData" />
		</div>
		-->
		<div
			class="col-span-3 h-80"
		>
			<LineChart :chartData="lineData" />
		</div>
	</div>
</template>

<script setup lang="ts">
const route = useRoute();

const chartData = ref({
	labels: ["January", "February", "March"],
	datasets: [
		{
			label: "Data One",
			backgroundColor: "#f87979",
			data: [40, 20, 12],
		},
	],
});

const lineData = ref({
	labels: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30],
	datasets: [
		{
			label: "My Data",
			backgroundColor: "rgba(75, 192, 192, 0.03)",
			data: [65, 59, 80, 81, 56, 55, 40, 55, 57, 60, 62, 65, 55, 57, 58, 64, 67, 72, 67, 67, 80, 77, 75, 76, 73, 81, 79, 82, 83, 83],
			borderColor: "rgba(75, 192, 192, 1)",
			borderWidth: 2,
			fill: true,
			pointBorderColor: "rgba(0, 0, 0, 0)",
			pointBackgroundColor: "rgba(0, 0, 0, 0)",
			pointHoverBackgroundColor: "rgba(255, 255, 255, 1)",
			pointHoverBorderWidth: 2,
			pointHoverBorderColor: "rgba(75, 192, 192, 1)",
		},
	],
});
</script>
