<template>
  <div class="container mx-auto mt-6">
    <h2 class="text-2xl font-semibold text-left mb-4">ADMIN DATA</h2>
    <div class="overflow-x-auto">
      <table
        class="min-w-full bg-white border border-gray-200 shadow-lg rounded-lg"
      >
        <thead>
          <tr class="bg-gray-100 border-b">
            <th class="px-4 py-2 text-left text-gray-600 font-semibold">
              Name
            </th>
            <th class="px-4 py-2 text-left text-gray-600 font-semibold">
              Position
            </th>
            <th class="px-4 py-2 text-left text-gray-600 font-semibold">
              Office
            </th>
            <th class="px-4 py-2 text-left text-gray-600 font-semibold">Age</th>
            <th class="px-4 py-2 text-left text-gray-600 font-semibold">
              Start Date
            </th>
            <th class="px-4 py-2 text-left text-gray-600 font-semibold">
              Salary
            </th>
          </tr>
        </thead>
        <tbody>
          <tr class="border-b hover:bg-gray-50">
            <td class="px-4 py-2 text-gray-700">Tiger Nixon</td>
            <td class="px-4 py-2 text-gray-700">System Architect</td>
            <td class="px-4 py-2 text-gray-700">Edinburgh</td>
            <td class="px-4 py-2 text-gray-700">61</td>
            <td class="px-4 py-2 text-gray-700">2011/04/25</td>
            <td class="px-4 py-2 text-gray-700">$320,800</td>
          </tr>
          <tr class="border-b hover:bg-gray-50">
            <td class="px-4 py-2 text-gray-700">Jane Doe</td>
            <td class="px-4 py-2 text-gray-700">Product Manager</td>
            <td class="px-4 py-2 text-gray-700">New York</td>
            <td class="px-4 py-2 text-gray-700">29</td>
            <td class="px-4 py-2 text-gray-700">2019/08/12</td>
            <td class="px-4 py-2 text-gray-700">$120,000</td>
          </tr>
          <tr class="border-b hover:bg-gray-50">
            <td class="px-4 py-2 text-gray-700">John Smith</td>
            <td class="px-4 py-2 text-gray-700">Software Engineer</td>
            <td class="px-4 py-2 text-gray-700">San Francisco</td>
            <td class="px-4 py-2 text-gray-700">35</td>
            <td class="px-4 py-2 text-gray-700">2016/02/15</td>
            <td class="px-4 py-2 text-gray-700">$150,000</td>
          </tr>
          <!-- Add more rows as needed -->
        </tbody>
      </table>
    </div>
  </div>
</template>
<script setup></script>

<style></style>
