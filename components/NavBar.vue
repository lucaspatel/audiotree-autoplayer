<template>
  <div class="w-full">
    <nav class="flex items-center justify-between flex-wrap p-6" :class="'bg-' + color + '-500'">
      <div class="flex items-center flex-shrink-0 text-white mr-6">
        <svg class="fill-current h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54" xmlns="http://www.w3.org/2000/svg">
          <path d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z"/>
        </svg>
        <span class="font-semibold text-xl tracking-tight"> Audiotree Autoplayer </span>
      </div>
      <div class="block lg:hidden">
        <button @click="open = !open" class="flex items-center px-3 py-2 border rounded hover:text-white hover:border-white" :class="['text-' + color + '-200', 'border-' + color + '-400']">
          <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <title>Menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div :class="open ? 'block': 'hidden'" class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
        <div class="text-sm lg:flex-grow">
          <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 hover:text-white mr-4" :class="'text-' + color + '-200'"> One </a>
          <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 hover:text-white mr-4" :class="'text-' + color + '-200'"> Two </a>
          <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 hover:text-white mr-4" :class="'text-' + color + '-200'"> Three </a>
        </div>
        <div>
          <a href="#" class="inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:bg-white mt-4 lg:mt-0" :class="'hover:text-' + color + '-500'"> Button </a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  props: ['color'],
  data() {
  	return {
      open: false
    }
  }
}
</script>

<style>
</style>
