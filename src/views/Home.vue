<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
import UserLayouts from '@/layouts/UserLayouts.vue'
import { HandHelp, Leaf, Seedling } from '@/stores/icon'
import { ref } from 'vue'

const items = ref([
  {
    icon: Seedling,
    title: 'គុណភាពខ្ពស់',
    description: 'យើងផ្តល់ផលិតផលកសិកម្មដែលមានគុណភាពខ្ពស់ និងស្តង់ដារអន្តរជាតិ។',
  },
  {
    icon: HandHelp,
    title: 'ការគាំត្រកសិករ',
    description: 'យើងផ្តល់ការប្រឹក្សា និងគាំទ្របច្ចេកទេសដល់កសិករដើម្បីបង្កើនទិន្នផល។',
  },
  {
    icon: Leaf,
    title: 'កសិកម្មប្រកបដោយចីរភាព',
    description: 'យើងលើកកម្ពស់ការអនុវត្តកសិកម្មដែលថែរក្សាបរិស្ថាន និងធនធានធម្មជាតិ។',
  },
])
</script>
<template>
  <UserLayouts>
    <!-- Image slider--app -->
    <div class="w-full relative">
      <img
        src="https://www.cnc.com.kh/news/62ecd34464a73.jpeg"
        class="w-full h-100 object-top object-cover"
        alt=""
      />

      <!--  -->
      <span
        class="absolute top-0 right-0 bottom-0 left-0 bg-black/40 text-shadow-md flex justify-center items-center flex-col text-white gap-3"
      >
        <h1 class="text-5xl font-bold text-shadow-md">ផលិតផលកសិកម្មដែលមានគុណភាពខ្ពស់</h1>
        <p class="font-medium text-xl">ដំណោះស្រាយដ៏ល្អបំផុតសម្រាប់កសិករខ្មែរ</p>
        <router-link to="#">
          <button
            class="mt-3 bg-amber-400 hover:bg-amber-500 text-white text-lg font-semibold px-6 py-2 rounded-full shadow-lg transition-all duration-300"
          >
            ទំនិញរបស់ពួកយើង
          </button>
        </router-link>
      </span>
    </div>
    <!-- End Image slider--app -->
    <!-- block ifo -->
    <!-- block info -->
    <section class="w-full py-12 px-6 font-khmer">
      <div class="mx-auto grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
        <!-- image -->
        <div class="w-full">
          <img
            src="https://www.cnc.com.kh/news/f71d94d437e7bcc832ffbb8759e76f93.jpg"
            alt="អំពីក្រុមហ៊ុន"
            class="rounded-2xl h-[500px] shadow-lg w-full object-cover"
          />
        </div>

        <!-- info -->
        <div class="space-y-4">
          <h1 class="text-2xl md:text-3xl font-bold text-success-dark">អំពីពួកយើង</h1>
          <p class="text-gray-700 leading-relaxed text-lg">
            ប្រេន ឥន្ទ្រីមាស មានផ្គត់ផ្គង់ និងចែកចាយជី ថ្នាំសម្លាប់សត្វល្អិតក្នុង 24 ខេត្ត។
            ហើយបានចាប់ផ្តើមដំណើរការជាផ្លូវការនៅឆ្នាំ 2020
            ដោយក្រុមហ៊ុនបាននាំចូលផ្តាច់ផ្ដាច់នូវជីដែលមានគុណភាពខ្ពស់ - ថ្នាំសម្លាប់សត្វល្អិត រូបមន្ត
            និងបច្ចេកវិទ្យាចុងក្រោយបង្អស់ពីប្រទេសឥណ្ឌា អេស្ប៉ាញ និងប្រទេសចិន។
          </p>

          <p class="text-gray-700 leading-relaxed text-lg">
            ចក្ខុវិស័យរបស់យើង គឺជួយកសិករ​ខ្មែរ​ឲ្យ​ធ្វើ​កសិកម្មកាត់បន្ថយការចំណាយ
            និងទទួលបានទិន្នផលច្រើនជាងការរំពឹងទុក។
          </p>
          <p class="text-gray-700 leading-relaxed text-lg">
            បេសកកម្មរបស់យើង គឺប្រឹក្សាបច្ចេកទេសកសិកម្ម និង ផ្គត់ផ្គង់ និងចែកចាយជីដែលមានគុណភាពខ្ពស់។
          </p>

          <button
            class="bg-success hover:bg-success-dark text-lg font-semibold text-white px-6 py-3 rounded-lg shadow transition duration-200"
          >
            ផលិតផលរបស់ពួកយើង
          </button>
        </div>
      </div>
    </section>
    <!--  -->

    <h1 class="text-2xl w-full text-center md:text-3xl font-bold text-success-dark mb-10">
      បេសកកម្មរបស់យើង
    </h1>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 p-4 pt-0">
      <!-- card 1 -->
      <div
        v-for="(item, index) in items"
        :key="index"
        class="bg-white shadow-md rounded-lg p-8 text-center hover:shadow-lg transition"
      >
        <!-- icon -->
        <div class="flex justify-center mb-4">
          <!-- <i class="fas fa-award text-green-600 text-4xl"></i> -->
          <component :is="item.icon" class="w-14 h-14 text-success" />
        </div>
        <h1 class="text-2xl text-success-dark font-bold mb-2">{{ item.title ?? 'null' }}</h1>
        <p class="text-gray-600">{{ item.description ?? 'null' }}</p>
      </div>
    </div>

    <!--  -->
    <!-- contact block -->
    <section class="w-full p-4 mt-8 mb-14">
      <div class="mx-auto text-center space-y-6 bg-white shadow-md rounded-lg py-8 px-6 font-khmer">
        <h1 class="text-3xl font-bold text-success-dark">ទំនាក់ទំនងជាមួយពួកយើង</h1>
        <p class="max-w-2xl mx-auto text-lg">
          ប្រសិនបើអ្នកមានសំណួរ ឬត្រូវការជំនួយ ក្រុមការងាររបស់យើងរួចរាល់ក្នុងការជួយអ្នក
          សូមទាក់ទងមកពួកយើង ដើម្បីទទួលបានការឆ្លើយតបដែលលឿន និងមានប្រសិទ្ធភាព។
        </p>
        <button
          class="bg-success-dark text-lg text-white px-6 py-3 rounded-full font-semibold shadow-lg hover:bg-success transition duration-200"
        >
          ទាក់ទងឥឡូវនេះ
        </button>
      </div>
    </section>
  </UserLayouts>
</template>
