<template>
  <div>
    <button
      @click="toggleSidebar"
      class="visible lg:invisible fixed top-4 left-5 p-2 text-gray-900 bg-white border rounded-full focus:outline-none hover-button z-50"
    >
      <span class="sr-only">Open sidebar</span>
      <svg
        class="w-6 h-6"
        aria-hidden="true"
        fill="currentColor"
        viewBox="0 0 20 20"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          clip-rule="evenodd"
          fill-rule="evenodd"
          d="M2 4.75A.75.75 0 012.75 4h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 4.75zm0 10.5a.75.75 0 01.75-.75h7.5a.75.75 0 010 1.5h-7.5a.75.75 0 01-.75-.75zM2 10a.75.75 0 01.75-.75h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 10z"
        ></path>
      </svg>
    </button>
    <aside
      v-show="isSidebarOpen"
      class="fixed top-0 left-0 pt-10 h-screen w-64 bg-[#02298A] transition-transform ease-in-out transform z-40"
      :class="{ 'hidden md:block': !isSidebarOpen }"
    >
      <div class="h-full px-3 pb-4 overflow-hidden bg-[#02298A]">
        <div class="flex justify-center text-blue-200 text-xl font-extrabold">
          <div class="text-blue-600">ADO</div>
          VELOPERS
        </div>
        <ul class="space-y-2 font-medium mt-8">
          <li>
            <nuxt-link
              to="/admin/dashboard"
              class="flex items-center py-3 p-2 my-5 w-full text-slate-100 pl-5 rounded-l-full hover:bg-blue-500 duration-200 ms-5"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="1.5em"
                height="1.5em"
                viewBox="0 0 24 24"
              >
                <g
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="1.5"
                >
                  <path
                    d="M12 4v4M4 8l2.5 2.5m11 0L20 8M3 17h3m6 0l1-6m5 6h3M8.5 20.001H4A9.96 9.96 0 0 1 2 14C2 8.477 6.477 4 12 4s10 4.477 10 10c0 2.252-.744 4.33-2 6.001L15.5 20"
                  />
                  <path d="M12 23a3 3 0 1 0 0-6a3 3 0 0 0 0 6" />
                </g>
              </svg>
              <span class="ms-3 font-normal">Dashboard</span>
            </nuxt-link>
          </li>
          <!-- <li>
            <nuxt-link
              to="/admin/products"
              class="flex items-center py-3 p-2 my-5 w-full text-slate-100 pl-5 rounded-l-full hover:bg-blue-500 duration-200 ms-5"
            >
              <svg
                width="1.5em"
                height="1.5em"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M0.4375 0.1875H1.125H14.875H15.5625V0.875V14.625V15.3125H14.875H1.125H0.4375V14.625V0.875V0.1875ZM1.8125 1.5625V7.0625H7.3125V1.5625H1.8125ZM8.6875 1.5625V7.0625H14.1875V1.5625H8.6875ZM1.8125 8.4375V13.9375H7.3125V8.4375H1.8125ZM8.6875 8.4375V13.9375H14.1875V8.4375H8.6875Z"
                  fill="white"
                />
              </svg>

              <span class="flex-1 ms-1 whitespace-nowrap font-normal"
                >Products</span
              >
              
            </nuxt-link>
          </li> -->
          <li>
            <nuxt-link
              to="/admin/gifts"
              class="flex items-center py-3 p-2 my-5 w-full text-slate-100 pl-5 rounded-l-full hover:bg-blue-500 duration-200 ms-5"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="1.45em"
                height="1.45em"
                viewBox="0 0 24 24"
              >
                <path
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 12h.01M4 6h.01M4 18h.01M8 18h2m-2-6h2M8 6h2m4 0h6m-6 6h6m-6 6h6"
                />
              </svg>

              <span class="flex-1 ms-3 whitespace-nowrap font-normal"
                >Logs</span
              >
              <!-- <span class="inline-flex items-center justify-center w-3 h-3 p-3 ms-3 text-sm font-medium text-blue-800 bg-blue-100 rounded-full dark:bg-blue-900 dark:text-blue-300">3</span> -->
            </nuxt-link>
          </li>
          <li>
            <nuxt-link
              to="/admin/categories"
              class="flex items-center py-3 p-2 my-5 w-full text-slate-100 pl-5 rounded-l-full hover:bg-blue-500 duration-200 ms-5"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="1.5em"
                height="1.5em"
                viewBox="0 0 32 32"
              >
                <path
                  fill="currentColor"
                  d="M28.707 19.293L26 16.586V13a10.014 10.014 0 0 0-9-9.95V1h-2v2.05A10.014 10.014 0 0 0 6 13v3.586l-2.707 2.707A1 1 0 0 0 3 20v3a1 1 0 0 0 1 1h7v.777a5.15 5.15 0 0 0 4.5 5.199A5.006 5.006 0 0 0 21 25v-1h7a1 1 0 0 0 1-1v-3a1 1 0 0 0-.293-.707M19 25a3 3 0 0 1-6 0v-1h6Zm8-3H5v-1.586l2.707-2.707A1 1 0 0 0 8 17v-4a8 8 0 0 1 16 0v4a1 1 0 0 0 .293.707L27 20.414Z"
                />
              </svg>

              <span class="flex-1 ms-3 whitespace-nowrap font-normal"
                >Notifications</span
              >
            </nuxt-link>
          </li>
          <button
            @click="toggleDropdown"
            id="dropdownDefaultButton"
            data-dropdown-toggle="dropdown"
            class="flex items-center py-3 p-2 my-5 w-full text-slate-100 pl-5 rounded-l-full hover:bg-blue-500 duration-200 ms-5"
            type="button"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="me-2"
              width="1.75em"
              height="1.75em"
              viewBox="0 0 24 24"
            >
              <path
                fill="currentColor"
                d="M12 4a4 4 0 0 1 4 4a4 4 0 0 1-4 4a4 4 0 0 1-4-4a4 4 0 0 1 4-4m0 2a2 2 0 0 0-2 2a2 2 0 0 0 2 2a2 2 0 0 0 2-2a2 2 0 0 0-2-2m0 7c2.67 0 8 1.33 8 4v3H4v-3c0-2.67 5.33-4 8-4m0 1.9c-2.97 0-6.1 1.46-6.1 2.1v1.1h12.2V17c0-.64-3.13-2.1-6.1-2.1"
              />
            </svg>
            Users
            <svg
              class="w-2.5 h-2.5 ms-3"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 10 6"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="m1 1 4 4 4-4"
              />
            </svg>
          </button>

          <!-- Dropdown menu -->
          <div
            v-if="isOpen"
            class="translate-x-8 z-10 bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700"
          >
            <ul
              class="py-2 text-sm text-gray-700 dark:text-gray-200"
              aria-labelledby="dropdownDefaultButton"
            >
              <li>
                <nuxt-link
                  to="/admin/users/admin"
                  class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                  >Admin</nuxt-link
                >
              </li>
              <li>
                <a
                  href="#"
                  class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                  >Employees</a
                >
              </li>
            </ul>
          </div>
        </ul>
      </div>
    </aside>
  </div>
</template>

<script setup>
const isOpen = ref(false);

// Toggle function to switch the dropdown state
const toggleDropdown = () => {
  isOpen.value = !isOpen.value;
};

const isSidebarOpen = ref(true);

const toggleSidebar = () => {
  isSidebarOpen.value = !isSidebarOpen.value;
};

// Handle sidebar visibility based on screen size
const handleResize = () => {
  isSidebarOpen.value = window.innerWidth >= 1024; // 768 is the md breakpoint
};

// Attach event listener on component mount
onMounted(() => {
  handleResize();
  window.addEventListener("resize", handleResize);
});

// Remove event listener on component unmount
onBeforeUnmount(() => {
  window.removeEventListener("resize", handleResize);
});
</script>

<style scoped>
.hover-button {
  background-color: #f4f4f4;
  color: #28363d;
}
</style>
