<template>
  <div v-if="isOpen">
    <div
      class="fixed bg-zinc-400 bg-opacity-50 inset-0 flex items-center justify-center z-50"
    >
      <div v-motion-pop-visible class="bg-white shadow-lg rounded-lg p-3 pb-10">
        <div class="border-b-2 pb-1 border-blue-300">
          <div class="text-md">Place Your Finger on the Sensor</div>
          <div class="text-xs mb-1">Fingerprint sensor ready...</div>
        </div>
        <div class="flex justify-center py-5">
          <svg
            width="60"
            height="60"
            viewBox="0 0 60 60"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M55 27.7V30C54.9969 35.391 53.2513 40.6367 50.0233 44.9545C46.7954 49.2724 42.2582 52.4312 37.0884 53.9597C31.9186 55.4883 26.3931 55.3047 21.3362 53.4364C16.2792 51.5681 11.9616 48.1152 9.0274 43.5926C6.09317 39.07 4.69948 33.7201 5.05419 28.3407C5.40891 22.9614 7.49302 17.8408 10.9957 13.7426C14.4984 9.64451 19.232 6.78842 24.4905 5.60033C29.749 4.41224 35.2507 4.95581 40.175 7.14997"
              stroke="black"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M55 10L30 35.025L22.5 27.525"
              stroke="black"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>
        <div class="border-b-2 border-gray-200">
          <div class="mx-10 mb-5">
            <div class="text-sm text-center">
              Place your finger on the sensor for
            </div>
            <div class="text-sm text-center">
              the first scan. Keep it still.
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const emit = defineEmits();
const props = defineProps({
  isOpen: Boolean,
});

const cancelDelete = () => {
  emit("cancelled");
};
</script>

<style scoped></style>
