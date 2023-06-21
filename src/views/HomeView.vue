<template>
     <div class="pq">
       <p class="p"> {{ currentDateTime }}</p>
     </div>
</template>
   
<script>
   export default {
     data() {
       return {
         currentDateTime: ''
       };
     },
     mounted() {
       this.updateDateTime();
     },
     methods: {
       updateDateTime() {
         setInterval(() => {
           const currentDate = new Date();
           this.currentDateTime = currentDate.toLocaleString();
         }, 1000);
       }
     }
   };
</script>
   