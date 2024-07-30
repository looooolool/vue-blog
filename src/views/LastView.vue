<template>

<div class="float-left flex-1 border   border-slate-200 
w-82 rounded-sm
inset-x-2.5 inset-y-2.5 left-4 right-6 top-8 bottom-7 ml-2 mr-3 mt-2 
mb-2 shadow-sm  hover:shadow-md">

<img class=" shadow-transparent  ml-0.5 mr-0.5 mt-0.5 overflow-hidden"
src="../../src/assets/img/截屏2024-07-23 09.09.13.png" />
<p class="mt-5 ml-3 mb-2">文案壁纸</p>

<div class=" flex-1 ">
  <button class="float-left mt-1 ml-4 text-yellow-300 text-lg font-bold hover:text-yellow-400" 
  @click="increment">☆</button>
  <input class="mt-2 ml-1.5 mb-3 float-left text-neutral-300 text-sm " v-model="counter" type="text" />
  
</div>
<div class="flex-none float-none mt-12 mb-5 ml-4">
<img class=" w-9 h-9 mt-1 rounded-3xl float-left flex-1 
hover:w-10 hover:h-10 hover:mt-0.5 hover:mr-1 "
src="../../src/assets/img/user.png" />
<p class="ml-11 text-sm mb-1">一只浩瀚和烟海</p>
<p class="ml-11 text-sm text-neutral-500">发布到  壁纸/背景图/…</p>
</div>
</div> 



<div >

<div class="float-left flex-1 border   border-slate-200 h-72 rounded-sm
inset-x-2.5 inset-y-2.5 left-4 right-6 top-8 bottom-7 ml-2 mr-3 mt-2 
mb-2 shadow-sm  hover:shadow-md">
<img class=" shadow-transparent h-36 w-56 ml-0.5 mr-0.5 mt-0.5 overflow-hidden"
src="../../src/assets/img/截屏2024-07-23 09.09.13.png" />
<p class="mt-5 ml-3 mb-2">文案壁纸</p>
<div class=" flex-1 ">
  <div class="float-left mt-1 ml-4 text-yellow-300 text-lg font-bold">☆</div>
  <div class="mt-2 ml-1 mb-3 float-left text-neutral-300 text-sm ">21</div>
</div>
<div class="flex-none float-none mt-12 mb-5 ml-4">
<img class=" w-9 h-9 mt-1 rounded-3xl float-left flex-1"  src="../../src/assets/img/user.png" />
<p class="ml-11 text-sm mb-1">一只浩瀚和烟海</p>
<p class="ml-11 text-sm text-neutral-500">发布到  壁纸/背景图/…</p>
</div>
</div> 


<div class="float-left flex-1 border   border-slate-200 h-72 rounded-sm
inset-x-2.5 inset-y-2.5 left-4 right-6 top-8 bottom-7 ml-2 mr-3 mt-2 
mb-2 shadow-sm  hover:shadow-md">
<img class=" shadow-transparent h-36 w-56 ml-0.5 mr-0.5 mt-0.5 overflow-hidden"
src="../../src/assets/img/截屏2024-07-23 09.09.13.png" />
<p class="mt-5 ml-3 mb-2">文案壁纸</p>
<div class=" flex-1 ">
  <div class="float-left mt-1 ml-4 text-yellow-300 text-lg">☆</div>
  <div class="mt-2 ml-1 mb-3 float-left text-neutral-300 text-sm ">21</div>
</div>
<div class="flex-none float-none mt-12 mb-5 ml-4">
<img class=" w-9 h-9 mt-1 rounded-3xl float-left flex-1"  src="../../src/assets/img/user.png" />
<p class="ml-11 text-sm mb-1">一只浩瀚和烟海</p>
<p class="ml-11 text-sm text-neutral-500">发布到  壁纸/背景图/…</p>
</div>
</div> 
 </div>


</template>
<script>
export default {
  data() {
    return {
      counter: 8,
    };
  },
  methods: {
    increment() {
      this.counter += 1;
    },
  },
};
</script>

<style>



</style>