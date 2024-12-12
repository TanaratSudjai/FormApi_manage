<template>
  <div class="min-h-screen bg-gray-50 flex flex-col">
    <header class="bg-white shadow-md">
      <div
        class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center"
      >
        <div class="flex items-center">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-8 w-8 text-indigo-600 mr-3"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"
            />
          </svg>
          <span class="text-xl font-bold text-gray-800">Company Name</span>
        </div>
        <nav class="space-x-4">
          <a
            href="#"
            class="text-gray-600 hover:text-indigo-600 transition duration-300"
            >Home</a
          >
          <a
            href="#"
            class="text-gray-600 hover:text-indigo-600 transition duration-300"
            >About</a
          >
          <a
            href="#"
            class="text-gray-600 hover:text-indigo-600 transition duration-300"
            >Contact</a
          >
        </nav>
      </div>
    </header>

    <main class="flex-grow container mx-auto px-4 sm:px-6 lg:px-8 py-8">
      <div class="bg-white shadow-lg rounded-lg p-6">
        <div class="text-gray-500 text-sm mb-4 border-b pb-2 border-gray-200">
          <p>Some default layout content shared across all pages</p>
        </div>

        <div class="min-h-[400px]">
          <slot />
        </div>

        <div class="text-gray-500 text-sm mt-4 border-t pt-2 border-gray-200">
          <p>Some default layout content shared across all pages</p>
        </div>
      </div>
    </main>

    <footer class="bg-gray-800 text-white py-6">
      <div
        class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex justify-between items-center"
      >
        <p>&copy; 2024 Your Company. All rights reserved.</p>
        <div class="space-x-4">
          <a
            href="#"
            class="text-gray-300 hover:text-white transition duration-300"
            >Privacy Policy</a
          >
          <a
            href="#"
            class="text-gray-300 hover:text-white transition duration-300"
            >Terms of Service</a
          >
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "DefaultLayout",
  // You can add any necessary component logic here
};
</script>
