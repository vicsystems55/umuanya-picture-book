<template>
  <section class="container mx-auto pt-10">
    <!-- Total Signups -->
    <a
      href="#"
      class="block max-w-sm mx-auto text-center justify-center p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
    >
      <h5 class="mb-2 text-5xl font-bold tracking-tight text-gray-900 dark:text-white">
        {{ members.length }}
      </h5>
      <p class="font-normal text-gray-700 dark:text-gray-400">Total Sign Ups</p>
    </a>

    <!-- Export Buttons -->
    <div class="container py-5 text-center">
      <button
        type="button"
        class="text-white mr-5 bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
      >
        Export as Excel
      </button>
      <button
        type="button"
        class="text-white bg-orange-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
      >
        Export as PDF
      </button>
    </div>

    <!-- Members Table -->
    <div class="relative overflow-x-auto shadow-md sm:rounded-lg mt-8">
      <table class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400">
        <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
          <tr>
            <th scope="col" class="px-6 py-3">Image</th>
            <th scope="col" class="px-6 py-3">Fullname</th>
            <th scope="col" class="px-6 py-3">Status</th>
            <th scope="col" class="px-6 py-3">Age</th>
            <th scope="col" class="px-6 py-3">Expertise</th>
            <th scope="col" class="px-6 py-3">Action</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="member in members"
            :key="member.id"
            class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700"
          >
            <td class="px-6 py-4">
              <div class="relative w-10 h-10 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600">
                <img
                  v-if="member.profile_picture"
                  :src="member.profile_picture"
                  alt="Profile Picture"
                  class="absolute w-12 h-12 -left-1"
                />
                <svg
                  v-else
                  class="absolute w-12 h-12 text-gray-400 -left-1"
                  fill="currentColor"
                  viewBox="0 0 20 20"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill-rule="evenodd"
                    d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
                    clip-rule="evenodd"
                  ></path>
                </svg>
              </div>
            </td>
            <td class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
              {{ member.fullname }}
            </td>
            <td class="px-6 py-4">{{ member.status }}</td>
            <td class="px-6 py-4">{{ member.age_range }}</td>
            <td class="px-6 py-4">{{ member.expertise }}</td>
            <td class="px-6 py-4">
              <a
                href="#"
                class="font-medium text-blue-600 dark:text-blue-500 hover:underline"
                >Edit</a
              >
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      members: [],
    };
  },
  created() {
    this.fetchMembers();
  },
  methods: {
    fetchMembers() {
      axios
        .get(`${process.env.VUE_APP_URL}/api/umuanya-members`)
        .then((response) => {
          this.members = response.data;
        })
        .catch((error) => {
          console.error('Error fetching members:', error);
          alert('Failed to fetch members. Please try again later.');
        });
    },
  },
};
</script>
