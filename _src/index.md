---
title: Home
layout: base.njk
---

<is-land on:visible>

  <div id="counter" v-scope="{ count: 0 }">
    <p>Count: <span v-text="count"></span></p>
    <button @click="count++">Add one</button>
  </div>

  <template data-island>
    <script type="module">
      import { createApp } from './js/petite-vue.js'
      createApp().mount('#counter')
    </script>
  </template>

</is-land>

<is-land on:visible>
  <template data-island>
    <div id="scene-container"></div>
    <script type="module" src="js/threeScene.js"></script>
  </template>
</is-land>