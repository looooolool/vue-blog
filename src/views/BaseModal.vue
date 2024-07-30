<template>
  <Transition name="modal-outer">
  <div 
  v-show="modalActive" 
  class="absolute w-full bg-black bg-opacity-30 h-screen
      top-0 left-0 flex justify-center px-8">
      <Transition name="modal-inner">
      <div 
      v-if="modalActive"
       class="p-4 bg-slate-200 self-start mt-32 max-w-screen-md">
    
       <slot />
          <button 
          class=" text-gray-500 mt-8 bg-cyan-200 py-2 px-6"
          @click="$emit('close-modal')">
          Close        
          </button>
      </div>
    </Transition>
      </div>  
    </Transition>
    </template>
    
    <script>
   import { defineEmits } from 'vue';   
   import { defineProps } from 'vue';   
   defineEmits(["close-modal"]);
  
  defineProps({
    modalActive:{
        type:Boolean,
        default:false,
    }
  })
    </script>
  
    <style>
  .modal-outer-enter-active,
  .modal-outer-leave-active{
    transition: opacity 0.3s cubic-bezier(0.52,0.02,0.19,1.02);
  }
  .model-outer-enter-from,
  .modal-outer-leave-to{
    opacity:0;
  }
    </style>