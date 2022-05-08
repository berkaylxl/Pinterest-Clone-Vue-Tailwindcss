<template>
  <div class="px-3 py-4 flex items-center justify-between">
      <div class="flex items-center">
          <button class="rounded-full hover:bg-light p-3 items-center justify-center" type="button" name="button">
             <img src="./assets/images/logo.png" alt="logo" class="h-7 w-7">
          </button>
         <button v-for="item in tabItems" 
         :key="item" @click="selecTab=item.key" 
         :class="`${selectedTab===item.key ? 'bg-dark text-white' : 'text-dark hover:bg-light'} rounded-full py-3 px-5 font-semibold`"
         type="button">
             {{item.name}}
         </button>
      </div>
      <div class="flex-grow relative">
          <span class="material-icons absolute mt-3 ml-3 text-muted">search</span>
          <input class="text-muted w-full hover:bg-lightHover  rounded-full bg-ligt py-3 pr-3 pl-10" type="text" placeholder="Search">
      </div>
      <div class="flex items-center">
          <button type="button" class=" relative rounded-full hover:bg-light flex items-center justify-center p-3">
              <span class="material-icons text-3xl text-muted">notifications</span>
               <div class="rounded-full h-5 w-5 bg-primary text-white flex items-center justify-center absolute mb-6 ml-5 ">4</div>
          </button>
           <button type="button" class=" relative rounded-full hover:bg-light flex items-center justify-center p-3">
              <span class="material-icons text-3xl text-muted">textsms</span>
               <div class="rounded-full h-5 w-5 bg-primary text-white flex items-center justify-center absolute mb-6 ml-5 ">2</div>
          </button>
            <button class="rounded-full hover:bg-light p-3 items-center justify-center" type="button" name="button">
                 <img src="./assets/images/profil.jpg" alt="pp" class="rounded-full h-7 w-7 mb-1">
          </button>
      </div>
      <button type="button" class="rounded-full w-6 h-6 hover:bg-light flex items-center justify-center">
           <span class="material-icons text-muted">expand_more</span>
      </button>
  </div> 
</template>
<script>
export default {
     data() {
    return {
      tabItems: [
        {name: 'Home', key: 'home'},
        {name: 'Today', key: 'today'}
      ],
      selectedTab: 'home'
    }
  }
}
</script>

<style>

</style>