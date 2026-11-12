---
title: EduTools
layout: base.njk
permalink: edutools.html
---
List of good edutainment examples + their target audience, who uses them, where to play, etc. 

<is-land on:visible>

<div id="gallery" v-scope="{ active: 'all' }">
  <div class="filters">
    <button @click="active = 'all'" :class="{ on: active === 'all' }" :aria-pressed="active === 'all'">All</button>
    <button @click="active = 'gamecaps'" :class="{ on: active === 'gamecaps' }" :aria-pressed="active === 'gamecaps'">Game Footage</button>
    <button @click="active = 'gamebox'" :class="{ on: active === 'gamebox' }" :aria-pressed="active === 'gamebox'">Game Covers</button>
    <button @click="active = 'gameplat'" :class="{ on: active === 'gameplat' }" :aria-pressed="active === 'type'">Game Platforms</button>
  </div>
  <section class="topic" v-show="active === 'all' || active === 'gamecaps'">
    <h3>Game Footage</h3>
    <img src="img/gamecaps/simcity.jpeg" alt="Footage of SimCity Gameplay">
    <img src="img/gamecaps/WITWICS.png" alt="Footage of Carmen Sandiego Gameplay">
  </section>
  <section class="topic" v-show="active === 'all' || active === 'photos'">
    <h3>Game Covers</h3>
    <img src="img/gamebox/simcity.jpeg" alt="Simcity Game Cover">
    <img src="img/gamebox/WITWICS.jpeg" alt="Carmen Sandiego Game Cover">
  </section>
  <section class="topic" v-show="active === 'all' || active === 'type'">
    <h3>Type</h3>
    <img src="img/gameplat/steam.jpeg" alt="Steam Logo">
    <img src="img/gameplat/itch.png" alt="Itch.io Logo">
  </section>
</div>

  <template data-island>
    <script type="module">
      import { createApp } from './js/petite-vue.js'
      createApp().mount('#gallery')
    </script>
  </template>

</is-land>