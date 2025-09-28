<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
import { logoHY } from '@/stores/icon'
</script>

<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <!-- footer -->
  <footer class="w-full bg-success-dark text-white py-10 px-6 font-khmer">
    <div class="max-w-9xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-8">
      <!-- logo & company -->
      <div>
        <div class="flex items-center space-x-3 mb-4">
          <img :src="logoHY" alt="Company Logo" class="w-14 h-14 object-contain" />
          <div>
            <h2 class="text-xl font-bold leading-tight">ក្រុមហ៊ុន​ ហ៊ុយយន់ អេហ្គ្រីខលឈ័រ</h2>
            <p class="text-lg font-roboto-slab text-gray-300">Huy Yun Agriculture Co.,Ltd.</p>
          </div>
        </div>
        <p class="text-gray-300 text-md leading-relaxed font-medium">
          យើងជាក្រុមហ៊ុនកសិកម្ម ដែលផ្តោតលើផលិតផលមានគុណភាពខ្ពស់ និងស្តង់ដារអនាម័យ
          ដើម្បីបម្រើទីផ្សារកម្ពុជា និងអន្តរជាតិ។
        </p>
      </div>

      <!-- quick links -->
      <div>
        <h2 class="text-xl font-semibold mb-4">តំណភ្ជាប់រហ័ស</h2>
        <ul class="space-y-1 text-gray-300 text-md leading-relaxed font-medium">
          <li><a href="#" class="hover:text-white">ទំព័រដើម</a></li>
          <li><a href="#" class="hover:text-white">អំពីយើង</a></li>
          <li><a href="#" class="hover:text-white">ផលិតផល</a></li>
          <li><a href="#" class="hover:text-white">ទំនាក់ទំនង</a></li>
        </ul>
      </div>

      <!-- contact -->
      <div>
        <h2 class="text-xl font-semibold mb-4">ទំនាក់ទំនង</h2>
        <ul class="space-y-1 text-gray-100 text-md leading-relaxed font-medium">
          <li>អ៊ីមែល៖ info@huyyun-agri.com</li>
          <li>ទូរស័ព្ទ៖ +855 12 345 678</li>
          <li>អាសយដ្ឋាន៖ ភ្នំពេញ កម្ពុជា</li>
        </ul>
      </div>

      <!-- follow us -->
      <div>
        <h2 class="text-lg font-semibold mb-4">ស្វែងរកពួកយើង</h2>
        <!-- <div class="space-y-2 text-gray-300 text-sm mb-4">
          <p>ភូមិ/សង្កាត់: ទួលគោក</p>
          <p>ខណ្ឌ: ទួលគោក</p>
          <p>ក្រុង: ភ្នំពេញ, កម្ពុជា</p>
        </div> -->
        <!-- Google Map -->
        <!-- allowfullscreen="" -->
        <div class="w-full rounded overflow-hidden mb-10">
          <iframe
            class="w-full h-30"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3905.746651185788!2d104.90113311532872!3d11.568271347013045!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3109513c2f51f10d%3A0x6f4cb1d1c39c4d8!2sTuol%20Kouk%2C%20Phnom%20Penh!5e0!3m2!1sen!2skh!4v1695812345678"
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
      </div>
    </div>

    <!-- bottom bar -->
    <div class="border-t border-white pt-4 text-center text-gray-200 text-sm">
      © ២០២៥ ក្រុមហ៊ុន​ ហ៊ុយយន់ អេហ្គ្រីខលឈ័រ | Huy Yun Agriculture Co.,Ltd. | All Rights Reserved.
    </div>
  </footer>
</template>
