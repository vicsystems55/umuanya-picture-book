<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="flex justify-center pt-5">
    <div
      class="w-full max-w-xl p-4 bg-white border border-gray-200 rounded-lg shadow sm:p-6 md:p-8 dark:bg-gray-800 dark:border-gray-700"
    >
      <div class="space-y-6" >
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
            v-model="fullname"
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
            v-model="fathersname"
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
                v-model="status"
                :value="'Student'"
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
                v-model="status"
                :value="'Professional'"
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
                v-model="status"
                :value="'Others'"
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
                v-model="age_range"
                :value="'18-24'"
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
                 v-model="age_range"
                :value="'25-29'"
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
                v-model="age_range"
                :value="'40-59'"
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
                 v-model="age_range"
                :value="'above 60'"
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
            v-model="expertise"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
          >
            <option selected>Choose an area</option>
            <option :value="'Engineering'">Engineering</option>
            <option :value="'IT'">IT</option>
            <option :value="'Law'">Law</option>
            <option :value="'Social Science'">Social Science</option>
            <option :value="'Medicine'">Medicine</option>
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
            v-model="facebook_url"
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
            name="linkedin"
            v-model="linkedin_url"
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
            v-model="other_accounts_url"
            id="others"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            placeholder="Others please indicate"
          />
        </div>

        
        <div class="flex items-center justify-center w-full">
      <label
        for="dropzone-file"
        class="flex flex-col items-center justify-center w-full h-64 border-2 border-gray-300 border-dashed rounded-lg cursor-pointer bg-gray-50 dark:hover:bg-gray-800 dark:bg-gray-700 hover:bg-gray-100 dark:border-gray-600 dark:hover:border-gray-500 dark:hover:bg-gray-600"
      >
        <div class="flex flex-col items-center justify-center pt-5 pb-6" v-if="!preview">
          <svg
            class="w-8 h-8 mb-4 text-gray-500 dark:text-gray-400"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 20 16"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M13 13h3a3 3 0 0 0 0-6h-.025A5.56 5.56 0 0 0 16 6.5 5.5 5.5 0 0 0 5.207 5.021C5.137 5.017 5.071 5 5 5a4 4 0 0 0 0 8h2.167M10 15V6m0 0L8 8m2-2 2 2"
            />
          </svg>
          <p class="mb-2 text-sm text-gray-500 dark:text-gray-400">
            <span class="font-semibold">Click to upload profile picture</span>
          </p>
          <p class="text-xs text-gray-500 dark:text-gray-400">
            PNG, JPG or GIF (MAX. 800x400px)
          </p>
        </div>
        <img
          v-if="preview"
          :src="preview"
          alt="Uploaded Image"
          class="object-contain w-full h-full"
        />
        <input
          id="dropzone-file"
          type="file"
          class="hidden"
          accept="image/png, image/jpeg, image/gif"
          @change="handleFileUpload"
        />
      </label>
    </div>


        <button
          @click="registerMember"
          class="w-full text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
        >
          {{loading?'Please wait': 'Submit'}}
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      fullname: '',
      fathersname: '',
      status: '',
      expertise: '',
      age_range: '',
      facebook_url: '',
      linkedin_url: '',
      other_accounts_url: '',
      file: null,
      preview: null,
      loading: false,
    };
  },
  methods: {
    handleFileUpload(event) {
      const selectedFile = event.target.files[0];
      if (selectedFile) {
        this.file = selectedFile;
        this.preview = URL.createObjectURL(selectedFile); // Generate preview
      }
    },
    registerMember() {
      // Ensure all required data is filled
      if (!this.fullname || !this.status) {
        alert('Please fill in all required fields.');
        return;
      }

      this.loading = true; // Start the loading state

      // Prepare the FormData
      const formData = new FormData();
      formData.append('fullname', this.fullname);
      formData.append('fathersname', this.fathersname);
      formData.append('status', this.status);
      formData.append('expertise', this.expertise);
      formData.append('age_range', this.age_range);
      formData.append('facebook_url', this.facebook_url);
      formData.append('linkedin_url', this.linkedin_url);
      formData.append('other_accounts_url', this.other_accounts_url);
      if (this.file) {
        formData.append('profile_picture', this.file); // Assuming `this.file` holds the uploaded file
      }

      // Make the Axios POST request
      axios
        .post(`${process.env.VUE_APP_URL}/api/register-umuanya-member`, formData, {
          headers: {
            // 'Content-Type': 'application/json', // Required for FormData
          },
        })
        .then((response) => {
          alert('Registration successful!');
          console.log('Server Response:', response.data);

          // Reset form fields
          this.fullname = '';
          this.fathersname = '';
          this.status = '';
          this.expertise = '';
          this.age_range = '';
          this.facebook_url = '';
          this.linkedin_url = '';
          this.other_accounts_url = '';
          this.file = null;
          this.preview = null;

          // Optionally redirect to a success page
          this.$router.push('/registration-successful');
        })
        .catch((error) => {
          alert('no');
          console.log(error)
          // Handle server or network errors
          if (error.response) {
            // Server responded with a status outside the 2xx range
            alert(`Error: ${error.response.data.message || 'Something went wrong!'}`);
            console.error('Server Error:', error.response.data);
          } else if (error.request) {
            // Request was made, but no response was received
            alert('Network error: No response received.');
            console.error('Network Error:', error.request);
          } else {
            // Something else happened
            alert(`Error: ${error.message}`);
            console.error('Error:', error.message);
          }
        })
        .finally(() => {
          this.loading = false; // End the loading state
        });
    },
  },
};

</script>
