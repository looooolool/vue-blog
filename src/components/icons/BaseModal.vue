<template>
<div 
v-show="modalActive" class="absolute w-full bg-black bg-opacity-30 h-screen
    top-0 left-0 flex justify-center px-8">
    <div v-if="modalActive"
     class="p-4 bg-slate-200 self-start mt-32 max-w-screen-md">
  
     <slot />
        <button 
        class=" text-gray-500 mt-8 bg-cyan-200 py-2 px-6">
        Close
        </button>
    </div>
    </div>


    
  </template>
  
  <script>
//   defineProps({
//     modalActive:{
//         type:Boolean,
//         default:false,
//     }
//   })
  </script>

  <style>

  </style>