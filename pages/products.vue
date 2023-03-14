<template>
	<div class="flex-grow flex justify-center py-8">
		<div class="lg: max-w-[1200px] flex-grow">
			<div
				class="flex justify-between items-center px-6 mb-4"
			>
				<h2 class="text-2xl font-medium">Products</h2>
				<div class="flex gap-2">
					<button
						class="bg-[#232323] rounded-lg px-4 py-2"
					>
						Import</button
					><button
                                        @click="isOpen = true"
						class="bg-[#5F02BC] rounded-lg px-4 py-2"
					>
						Add a product
					</button>
				</div>
			</div>
			<div class="flex gap-2 items-center mb-4 px-6 pt-4">
				<input
					class="border border-[#363636] bg-transparent focus:outline-none focus:outline-[#5F02BC] focus:outline-offset-0 rounded-lg px-4 py-2 flex-grow text-left placeholder:text-white placeholder:opacity-30"
					placeholder="Search"
				/>
				<button
					class="border border-[#363636] rounded-lg px-4 py-2"
				>
					Import</button
				><button
					class="border border-[#363636] rounded-lg px-4 py-2"
				>
					Add a product
				</button>
			</div>

			<table
				class="table-fixed flex-grow flex flex-col items-stretch"
			>
				<thead class="flex-grow">
					<tr
						class="grid grid-cols-9 text-xs tracking-widest uppercase [&>*]:font-medium [&>*]:opacity-80 [&>*]:py-4 [&>*]:px-6 border-y border-[#232323]"
					>
						<th
							class="col-span-5 text-left flex items-center"
						>
							<div
								class="h-4 w-4 border border-[#454545] rounded mr-6 flex-none"
							></div>
							<span>Song</span>
						</th>
						<th
							class="col-span-2 text-left"
						>
							Artist
						</th>
						<th
							class="col-span-2 text-right"
						>
							Year
						</th>
					</tr>
				</thead>
				<tbody class="flex-grow">
					<tr
						v-for="i in 10"
						class="grid grid-cols-9 border-b border-[#232323] [&>*]:py-[10px] [&>*]:px-6 hover:bg-[#2323235d]"
					>
						<td
							class="col-span-5 text-left flex items-center"
						>
							<div
								class="h-4 w-4 border border-[#454545] rounded flex-none"
							></div>
							<div
								class="h-9 w-9 bg-[#232323] mx-6 rounded-md flex-none"
							></div>
							The Sliding Mr. Bones
							(Next Stop,
							Pottersville)
						</td>
						<td
							class="col-span-2 text-left opacity-80 items-center flex"
						>
							Malcolm Lockyer
						</td>
						<td
							class="col-span-2 opacity-80 items-center justify-end flex"
						>
							1961
						</td>
					</tr>
				</tbody>
			</table>
			<div class="flex justify-between items-center mt-2">
				<p class="text-xs py-4 px-6 opacity-80">
					Page 1 of 34
				</p>
				<div class="flex gap-2">
					<button
						class="bg-[#232323] rounded-lg px-4 py-2"
					>
						Prev</button
					><button
						class="bg-[#232323] rounded-lg px-4 py-2"
					>
						Next
					</button>
				</div>
			</div>
		</div>
		
	</div>
        <HeadlessTransitionRoot :show="isOpen" as="template">
                <HeadlessDialog :open="isOpen" @close="setIsOpen" class="relative z-50 text-sm">
                        <HeadlessTransitionChild
        enter="duration-300 ease-out"
        enter-from="opacity-0"
        enter-to="opacity-100"
        leave="duration-200 ease-in"
        leave-from="opacity-100"
        leave-to="opacity-0"
      >
                        <div class="fixed inset-0 bg-white/5" aria-hidden="true" />
                </HeadlessTransitionChild>
                        <div class="fixed inset-0 flex items-center justify-center p-4">
                                <HeadlessTransitionChild
        enter="duration-300 ease-out"
        enter-from="opacity-0 scale-95"
        enter-to="opacity-100 scale-100"
        leave="duration-200 ease-in"
        leave-from="opacity-100 scale-100"
        leave-to="opacity-0 scale-95"
      >
			<HeadlessDialogPanel class="w-full max-w-lg rounded-xl bg-[#111111] p-8 text-white border border-[#282828]">
				<HeadlessDialogTitle class="text-lg font-medium">Deactivate account</HeadlessDialogTitle
				>
				<HeadlessDialogDescription class="mb-4 text-red-500">
					This will permanently deactivate your
					account
				</HeadlessDialogDescription>

				<p class="opacity-60">
					Are you sure you want to deactivate your
					account? All of your data will be
					permanently removed. This action cannot
					be undone.
				</p>
                                <div class="flex gap-2 mt-6 justify-end">
				<button @click="setIsOpen(false)" class="px-4 py-2 rounded-md bg-[#232323]">
					Deactivate
				</button>
				<button @click="setIsOpen(false)" class="px-4 py-2 rounded-md bg-[#232323]">
					Cancel
				</button>
                        </div>
			</HeadlessDialogPanel>
                        </HeadlessTransitionChild>
                        </div>
		</HeadlessDialog>
        </HeadlessTransitionRoot>
</template>

<script setup>
const isOpen = ref(true);

function setIsOpen(value) {
	isOpen.value = value;
}
</script>
