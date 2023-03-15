<template>
	<div class="flex dark:bg-[#131313] dark:text-white text-sm">
		<Sidebar />
		<div class="flex-grow flex justify-center py-8">
			<div class="lg: max-w-[1200px] flex-grow">
		<slot />
	</div>
	</div>
	</div>
</template>
