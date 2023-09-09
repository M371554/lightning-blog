<template>
    <div >

            <div class="space-y-5 sm:space-y-4 text-center">
              <h2
                class="text-3xl font-bold tracking-tight sm:text-4xl text-colorTxtLight dark:text-colorTxtDark">
                {{ $t("homepage.title") }} !
              </h2>
              <p class="text-xl text-gray-500 dark:text-sky-400">
                <!-- {{ $t("homepage.subtitle") }} -->
                {{ $t("homepage.subtitle") }}
              </p>
            </div>
    
      
    </div>
    </template>
    
    <style >
    .path {
      animation: draw 5.5s infinite;
    }
     
     @keyframes draw {
      50% {
        stroke-dashoffset: 0;
      }
    }
    
    </style>