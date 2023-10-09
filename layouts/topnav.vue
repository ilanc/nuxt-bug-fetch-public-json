<template>
  <div>
    <nav class="bg-white border-b border-b-gray-300">
      <div class="px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16">
          <div class="flex">
            <div class="ml-6 flex space-x-8">
              <nuxt-link
                class="inline-flex items-center px-1 pt-1 border-b-2 text-sm font-medium"
                :class="$route.name === 'index' ? activeClass : inactiveClass"
                to="/"
              >
                a
              </nuxt-link>
              <nuxt-link
                class="inline-flex items-center px-1 pt-1 border-b-2 text-sm font-medium"
                :class="$route.name === 'b' ? activeClass : inactiveClass"
                to="/b"
              >
                b
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </nav>
    <div class="p-6">
      <NuxtPage />
    </div>
  </div>
</template>
<script setup>
const activeClass = "border-indigo-500 text-gray-900";
const inactiveClass = "border-transparent text-gray-500 hover:border-gray-300 hover:text-gray-700";
</script>
