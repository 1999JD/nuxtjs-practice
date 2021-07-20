<template>
  <header
    class="flex justify-between items-center border-b-2 p-4 text-gray-500 mx-auto"
  >
    <div>
      <NuxtLink to="/">
        logo
      </NuxtLink>
    </div>
    <ul class="flex space-x-10">
      <li class="">
        <NuxtLink to="/page1">
          page1
        </NuxtLink>
      </li>
      <li class="">
        <NuxtLink to="page2">
          page2
        </NuxtLink>
      </li>
      <li class="">
        <NuxtLink to="/params/1">
          page-params
        </NuxtLink>
      </li>
    </ul>
    <button class="rounded p-3 text-white bg-purple-500">
      <NuxtLink to="/layout2-page">
        see layout2
      </NuxtLink>
    </button>
  </header>
</template>
