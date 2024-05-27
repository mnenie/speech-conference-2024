<template>
  <div class="flex flex-wrap justify-center items-center w-full h-90" :class="[ $clicks !== 0 ? 'pt-16' : 'pt-12']">
    <TransitionGroup name="list">
      <div key="logos-vue-devtools" class="flex flex-col items-center">
        <img src="https://devtools.vuejs.org/logo.svg" class="w-56 mx-7" />
        <!-- <p class="text-2xl" v-if="$clicks >= 1">Vue Devtools</p> -->
      </div>
      <img
        src="https://firefox-source-docs.mozilla.org/_images/logo-developer-quantum.png"
        key="logos-firefox"
        class="w-36 mx-7"
        v-if="$clicks === 0"
      />
      <img
        src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSxBMxTwPxeiCFus2tzi5bAKii4GzutQgoK8VoM6w6jTomsOxF4ZXlHBdIB23dRlk2Q3Rk&usqp=CAU"
        key="logos-edge"
        class="w-36 mx-7"
        v-if="$clicks === 0"
      />
      <img
        src="https://cdn.worldvectorlogo.com/logos/google-pagespeed-insights-icon-2021-.svg"
        key="logos-page-speed"
        class="w-36 mx-7"
        v-if="$clicks === 0"
      />
      <img
        src="https://media.licdn.com/dms/image/C4D0BAQEs_Ukr_RAPpQ/company-logo_200_200/0/1654101330295/webpagetest_logo?e=2147483647&v=beta&t=GehjcFPrwItGZZeh3iA9zghJM6ey_UITXPuz22bBzP0"
        key="logos-web-page"
        class="w-44 mx-7 mr-0"
        v-if="$clicks === 0"
      />
      <div key="logos-chrome-devtools" class="flex flex-col items-center">
        <img src="https://logowik.com/content/uploads/images/google-chrome-dev4048.jpg" class="w-52 mx-7 ml-6" />
        <!-- <p class="text-2xl" v-if="$clicks >= 1">Chrome Devtools</p> -->
      </div>
    </TransitionGroup>
  </div>
</template>

<style>
.list-move,
.list-enter-active,
.list-leave-active {
  transition: all 0.5s ease;
}

.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateX(30px);
}

.list-leave-active {
  position: absolute;
}
</style>
