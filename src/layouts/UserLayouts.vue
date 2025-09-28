<script setup lang="ts">
import { logoHY } from '@/stores/icon'
import Footer from '@/widgets/Footer.vue'

import { ref } from 'vue'

const pages = ref([
  {
    path: '/',
    name: 'home',
    title: 'ទំព័រដើម',
  },
  {
    path: '/',
    name: 'about',
    title: 'អំពីពួកយើង',
  },
  {
    path: '/',
    name: 'products',
    title: 'ផលិតផល',
  },
  {
    path: '/',
    name: 'contact',
    title: 'ទំនាក់ទំនង',
  },
])
</script>

<template>
  <div
    class="w-full h-screen flex flex-col font-kantumruy-pro overflow-y-auto relative bg-gray-100"
  >
    <nav class="w-full sticky top-0 z-50">
      <div
        class="w-full bg-success-dark text-white flex items-center justify-between px-4 py-3 shadow-md"
      >
        <!-- block logo company -->
        <div class="flex items-center gap-4">
          <div class="w-14 h-14 border rounded-full overflow-hidden bg-white">
            <img :src="logoHY" alt="" />
          </div>
          <div>
            <h1 class="text-xl font-bold">ក្រុមហ៊ុន​ ហ៊ុយយន់ អេហ្គ្រីខលឈ័រ</h1>
            <p class="font-roboto-slab font-medium">Huy Yun Agriculture Co.,Ltd</p>
          </div>
        </div>
        <!-- end logo company -->

        <!-- block menu -->
        <ul>
          <li v-for="(item, index) in pages" :key="index" class="inline-block mx-3 relative">
            <router-link to="#">
              <div class="flex flex-col items-center">
                <p class="text-lg font-medium hover:text-amber-400">{{ item.title }}</p>
                <span
                  v-if="index === 0"
                  class="absolute -bottom-1 right-0 left-0 p-[2.5px] bg-amber-400 rounded-full"
                ></span>
              </div>
            </router-link>
          </li>
        </ul>
      </div>
    </nav>

    <!--  -->
    <main class="flex-1">
      <slot></slot>
    </main>
    <!--  -->
    <Footer />
  </div>
</template>
