<template>
  <div>
    <div class="grid grid-row-3 lg:grid-cols-3 gap-4">
      <div class="p-5 rounded-xl bg-white shadow-xl border">
        <div>
          <div class="flex justify-between">
            <span class="inline-block">
              <div class="text-gray-500 font-semibold text-sm lg:text-md">
                Total Users
              </div>
              <div class="font-bold text-xl">322342</div>
            </span>
            <span class="inline-block px-3 text-right">
              <div class="bg-violet-100 rounded-xl">
                <img class="p-2.5" :src="users" />
              </div>
            </span>
          </div>
        </div>
      </div>

      <div class="p-5 rounded-xl bg-white shadow-xl border">
        <div>
          <div class="flex justify-between">
            <span class="inline-block">
              <div class="text-gray-500 font-semibold text-sm lg:text-md">
                Total Logs
              </div>
              <div class="font-bold text-xl">999797</div>
            </span>
            <span class="inline-block px-3 text-right">
              <div class="bg-yellow-200 rounded-xl">
                <img class="p-2" :src="product" />
              </div>
            </span>
          </div>
        </div>
      </div>

      <div class="p-5 rounded-xl bg-white shadow-xl border">
        <div>
          <div class="flex justify-between">
            <span class="inline-block">
              <div class="text-gray-500 font-semibold text-sm lg:text-md">
                Total Notifications
              </div>
              <div class="font-bold text-xl">2348736238</div>
            </span>
            <span class="inline-block px-3 text-right">
              <div class="bg-orange-100 rounded-xl">
                <img class="p-1" :src="category" />
              </div>
            </span>
          </div>
        </div>
      </div>
    </div>
    <div class="py-5 px-1">
      <img class="w-full h-auto" :src="cspc" />
    </div>
  </div>
</template>

<script setup>
import users from "../../assets/svgs/user.svg";
import category from "../../assets/svgs/categories.svg";
import product from "../../assets/svgs/product.svg";
import cspc from "../../assets/svgs/cspc.svg";

// definePageMeta({
//   middleware: "admin",
// });
</script>

<style scoped></style>
