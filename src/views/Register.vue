<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="flex justify-center pt-5">
    <div
      class="w-full max-w-xl p-4 bg-white border border-gray-200 rounded-lg shadow sm:p-6 md:p-8 dark:bg-gray-800 dark:border-gray-700"
    >
      <form class="space-y-6" action="#">
        <h5 class="text-xl font-medium text-gray-900 dark:text-white">
          Sign in to our platform
        </h5>
        <div>
          <label
            for="email"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
            >Your full name</label
          >
          <input
            type="text"
            name="fullname"
            id="fullname"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            placeholder="Enter your fullname"
            required
          />
        </div>
        <div>
          <label
            for="fathers"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
            >Father's name</label
          >
          <input
            type="text"
            name="fathers"
            id="fathers"
            placeholder="Enter Father's name"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            required
          />
        </div>

        <div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
          <div class="">
            <label
              for="fathers"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
              >Status</label
            >
            <div class="flex items-center mb-4">
              <input
                id="default-radio-1"
                type="radio"
                value=""
                name="default-radio"
                class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                for="default-radio-1"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >Student</label
              >
            </div>
            <div class="flex items-center mb-4">
              <input
                checked
                id="default-radio-2"
                type="radio"
                value=""
                name="default-radio"
                class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                for="default-radio-2"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >Professional</label
              >
            </div>

            <div class="flex items-center">
              <input
                checked
                id="default-radio-2"
                type="radio"
                value=""
                name="default-radio"
                class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                for="default-radio-2"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >Others</label
              >
            </div>
          </div>
          <div class="">
            <label
              for="fathers"
              class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
              >Age Bracket</label
            >
            <div class="flex items-center mb-4">
              <input
                id="default-radio-1"
                type="radio"
                value=""
                name="age-bracket"
                class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                for="default-radio-1"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >18-24</label
              >
            </div>
            <div class="flex items-center mb-4">
              <input
                checked
                id="default-radio-2"
                type="radio"
                value=""
                name="age-bracket"
                class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                for="default-radio-2"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >25-29</label
              >
            </div>

            <div class="flex items-center mb-4">
              <input
                checked
                id="default-radio-2"
                type="radio"
                value=""
                name="age-bracket"
                class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                for="default-radio-2"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >40-59</label
              >
            </div>

            <div class="flex items-center">
              <input
                checked
                id="default-radio-2"
                type="radio"
                value=""
                name="age-bracket"
                class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
              />
              <label
                for="default-radio-2"
                class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                >60 plus</label
              >
            </div>
          </div>
        </div>

        <div class="mx-auto">
          <label
            for="expertise"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
            >Area of Expertise</label
          >
          <select
            id="expertise"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
          >
            <option selected>Choose an area</option>
            <option value="Engineering">Engineering</option>
            <option value="IT">IT</option>
            <option value="Law">Law</option>
            <option value="Social Science">Social Science</option>
            <option value="Medicine">Medicine</option>
          </select>
        </div>

        <label
          for="social"
          class="block mb-2 text-sm font-medium mt-2 text-gray-900 dark:text-white"
          >Social Media Handles</label
        >

        <div>
          <label
            for="facebook"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
            >Facebook:</label
          >
          <input
            type="text"
            name="facebook"
            id="facebook"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            placeholder="Facebook url"
          />
        </div>

        <div>
          <label
            for="linkedin"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
            >LinkedIn:</label
          >
          <input
            type="text"
            name="facebook"
            id="linkedin"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            placeholder="Facebook url"
          />
        </div>

        <div>
          <label
            for="others"
            class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
            >Others:</label
          >
          <input
            type="text"
            name="ohters"
            id="others"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            placeholder="Others please indicate"
          />
        </div>

        <button
          type="submit"
          class="w-full text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
        >
          Submit
        </button>
      </form>
    </div>
  </div>
</template>
