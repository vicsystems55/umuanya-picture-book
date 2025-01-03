<template>
    <section class="container mx-auto">
        
<div class="grid grid-cols-2 md:grid-cols-3 gap-4">

    <div 
       v-for="member in members"
        :key="member.id"
    >
        <img class="h-auto max-w-full rounded-lg" style="object-fit:cover; height: 300px; width: 300px;" :src="prepareUrl(member.image_url)" alt="">
        <h6 class="text-4xl font-black text-gray-900 dark:text-white">  {{ member.fullname }} </h6>
        
    </div>


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

