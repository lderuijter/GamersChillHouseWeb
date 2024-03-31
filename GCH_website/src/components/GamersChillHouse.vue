<template>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Honk&family=Micro+5&display=swap"
      rel="stylesheet"
    />
  </head>
  <div class="flex flex-row bg-white shadow-xl shadow-blue-500/50 rounded-b-lg">
    <div class="basis-1/2">
      <img class="float-left w-28 hidden xl:block" src="../assets/images/clan_logo.png" />
      <img class="float-right mx-5 w-48 hidden sm:block" src="../assets/images/10.png" />
    </div>
    <div class="basis-1/2">
      <h1 class="float-left font-honk text-5xl text-black w-fit mx-5 my-7">GamersChillHouse</h1>
      <img class="float-right w-28 hidden xl:block" src="../assets/images/clan_logo.png" />
    </div>
  </div>
  <div class="flex flex-row">
    <div class="basis-1/3 hidden md:block bg-gray-950 mr-5 shadow-lg shadow-blue-500/50">
      <h1 class="font-honk text-5xl text-black text-center mx-5 my-7">
        <a target="_blank" href="https://warframe.market/">Warframe Market</a>
      </h1>
      <p class="text-center mx-8 text-white font-mono h-fit text-wrap">
        De link hierboven lijd je naar een site waar je in game items kan kopen en verkopen met
        platinum. Zo kan je bijvoorbeeld mods farmen om platinum te verdienen en daar kan je dan
        weer warframes van halen of andere mods van halen.
      </p>
      <h1 class="font-honk text-5xl text-black text-center mx-auto my-7">Extra</h1>
    </div>
    <div class="sm:basis-1/3">
      <h1 class="font-honk text-5xl text-black text-center mx-5 my-7">Messages</h1>
      <div class="bg-blue-900 shadow-lg shadow-blue-500/50 rounded-lg mb-10">
        <div class="text-center text-white font-mono h-fit text-wrap">
          <h1 class="text-center text-lg">1</h1>
          <h1 class="text-2xl">Message sample</h1>
          <p class="text-lg">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus pretium risus at
            aliquet porta. Quisque ut luctus sapien. Aliquam posuere hendrerit faucibus. Lorem ipsum
            dolor sit amet, consectetur adipiscing elit. Donec quis justo vitae magna dignissim
            ornare. Fusce sagittis ornare nisl, et accumsan magna pretium ut. Sed consequat nunc sed
            suscipit tincidunt. Donec egestas placerat magna, sed auctor est euismod id.
          </p>
        </div>
      </div>
      <div class="bg-blue-900 shadow-lg shadow-blue-500/50 rounded-lg mb-10">
        <div class="text-center text-white font-mono h-fit text-wrap">
          <h1 class="text-center text-lg">2</h1>
          <h1 class="text-2xl">Message sample</h1>
          <p class="text-lg">
            Nullam suscipit non metus vel rhoncus. Ut porttitor, felis sit amet euismod gravida,
            tellus arcu vehicula nunc, eget rhoncus massa velit ac nisi. Proin eu sollicitudin dui.
            Donec aliquet quam ac felis sagittis convallis. Vivamus dignissim pellentesque elit at
            tristique. Vestibulum convallis tortor vel enim sodales blandit. Nam eu lectus sit amet
            urna congue sagittis. Phasellus nulla diam, blandit eu est vitae, porta scelerisque
            lectus. Integer mollis euismod quam eu commodo.
          </p>
        </div>
      </div>
      <div class="bg-blue-900 shadow-lg shadow-blue-500/50 rounded-lg mb-10">
        <div class="text-center text-white font-mono h-fit text-wrap">
          <h1 class="text-center text-lg">3</h1>
          <h1 class="text-2xl">Message sample</h1>
          <p class="text-lg">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus pretium risus at
            aliquet porta. Quisque ut luctus sapien. Aliquam posuere hendrerit faucibus. Lorem ipsum
            dolor sit amet, consectetur adipiscing elit. Donec quis justo vitae magna dignissim
            ornare. Fusce sagittis ornare nisl, et accumsan magna pretium ut. Sed consequat nunc sed
            suscipit tincidunt. Donec egestas placerat magna, sed auctor est euismod id.
          </p>
        </div>
      </div>
      <div class="bg-blue-900 shadow-lg shadow-blue-500/50 rounded-lg mb-10">
        <div class="text-center text-white font-mono h-fit text-wrap">
          <h1 class="text-center text-lg">4</h1>
          <h1 class="text-2xl">Message sample</h1>
          <p class="text-lg">
            Nullam suscipit non metus vel rhoncus. Ut porttitor, felis sit amet euismod gravida,
            tellus arcu vehicula nunc, eget rhoncus massa velit ac nisi. Proin eu sollicitudin dui.
            Donec aliquet quam ac felis sagittis convallis. Vivamus dignissim pellentesque elit at
            tristique. Vestibulum convallis tortor vel enim sodales blandit. Nam eu lectus sit amet
            urna congue sagittis. Phasellus nulla diam, blandit eu est vitae, porta scelerisque
            lectus. Integer mollis euismod quam eu commodo.
          </p>
        </div>
      </div>
    </div>
    <div class="basis-1/3 hidden md:block bg-gray-950 ml-5 shadow-lg shadow-blue-500/50">
      <h1 class="font-honk text-5xl text-black text-left mx-5 my-7">Admins</h1>
      <ul class="text-left mx-8 text-white font-mono h-fit text-wrap text-2xl">
        <li class="list-disc list-inside">Quin</li>
        <li class="list-disc list-inside">Marcel</li>
        <li class="list-disc list-inside">Lucas</li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts"></script>
