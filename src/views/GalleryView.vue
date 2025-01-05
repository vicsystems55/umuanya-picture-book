<template>
    <section class="container mx-auto">

      <div class="container h-58">
        <h2 class="text-5xl text-center mb-2 py-5">Picture Book</h2>

      </div>

        
<div class="grid grid-cols-2 md:grid-cols-3 gap-4">


  
<a    
v-for="member in members"
:key="member.id"
 href="#" class="flex flex-col items-center bg-white border border-gray-200 rounded-lg shadow md:flex-row md:max-w-xl hover:bg-gray-100 dark:border-gray-700 dark:bg-gray-800 dark:hover:bg-gray-700">
    <img class="object-cover w-full rounded-t-lg h-96 md:h-auto md:w-48 md:rounded-none md:rounded-s-lg" :src="prepareUrl(member.image_url)" alt="">
    <div class="flex flex-col justify-between p-4 leading-normal">
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ member.fullname }}</h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
          {{member.marital_status}}
        </p>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
          {{member.phone}}
        </p>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
          {{member.status}}
        </p>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
          {{member.age_range}}
        </p>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
          {{member.expertise}}
        </p>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
          {{member.address}}
        </p>
    </div>
</a>


    <!-- <div 
       v-for="member in members"
        :key="member.id"
    >
        <img class="h-auto max-w-full rounded-lg" style="object-fit:cover; height: 300px; width: 300px;" :src="prepareUrl(member.image_url)" alt="">
        <h6 class="text-4xl font-black text-gray-900 dark:text-white">  {{ member.fullname }} </h6>
        
    </div> -->


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

    prepareUrl(img){
      return process.env.VUE_APP_URL+'/storage/'+img;
    },

    fetchMembers() {
      axios
        .get(`${process.env.VUE_APP_URL}/api/umuanya-members`)
        .then((response) => {
          this.members = response.data;
          console.log(response.data)
        })
        .catch((error) => {
          console.error('Error fetching members:', error);
          alert('Failed to fetch members. Please try again later.');
        });
    },
  },
};
</script>

