<template>
        <div class="w-[16rem] border-r border-[#282828] h-screen hidden lg:flex flex-col p-4 flex-none sticky top-0">
        <h1 class="p-2 text-2xl font-bold">runcit</h1>
        <div class="mt-16"></div>
                <NuxtLink to="/"><div :class="`h-[38px] flex items-center px-4 gap-4 hover:opacity-100 rounded-lg ${route.name == 'index' ? 'bg-[#232323] opacity-100' : 'opacity-50'}`"><Icon name="lucide:home" size="1.25rem" />Home</div></NuxtLink>
                <NuxtLink to="/orders"><div :class="`h-[38px] flex items-center px-4 gap-4 hover:opacity-100 rounded-lg ${route.name == 'orders' ? 'bg-[#232323] opacity-100' : 'opacity-50'}`"><Icon name="lucide:truck" size="1.25rem" />Orders</div></NuxtLink>
                <NuxtLink to="/customers"><div :class="`h-[38px] flex items-center px-4 gap-4 hover:opacity-100 rounded-lg ${route.name == 'customers' ? 'bg-[#232323] opacity-100' : 'opacity-50'}`"><Icon name="lucide:users" size="1.25rem" />Customers</div></NuxtLink>
                <NuxtLink to="/products"><div :class="`h-[38px] flex items-center px-4 gap-4 hover:opacity-100 rounded-lg ${route.name == 'products' ? 'bg-[#232323] opacity-100' : 'opacity-50'}`"><Icon name="lucide:package-search" size="1.25rem" />Products</div></NuxtLink>
                <NuxtLink to="/settings"><div :class="`h-[38px] flex items-center px-4 gap-4 hover:opacity-100 rounded-lg ${route.name == 'settings' ? 'bg-[#232323] opacity-100' : 'opacity-50'}`"><Icon name="lucide:settings" size="1.25rem" />Settings</div></NuxtLink>
                <p class="text-xs tracking-widest uppercase opacity-40 px-4 mt-6 mb-2">Sales Channel</p>
                <NuxtLink to="/website"><div :class="`h-[38px] flex items-center px-4 gap-4 hover:opacity-100 rounded-lg ${route.name == 'website' ? 'bg-[#232323] opacity-100' : 'opacity-50'}`"><Icon name="lucide:shopping-cart" size="1.25rem" />Website</div></NuxtLink>
        </div>
</template>

<script setup lang="ts">
const route = useRoute();

const path = route.path;

</script>