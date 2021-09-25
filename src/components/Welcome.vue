<template>
  <header class="m-5">
    <h1 class="text-5xl">{{ msg }}</h1>
    <p>Ceci est un composant "Welcome" avec une variable (props) msg (qui contient le message: {{ msg }})</p>

    <button @click="seen=!seen;show=!show" v-if="show" class="bg-red-500 hover:bg-red-300 rounded p-2 text-white my-5">Show More</button>
    <button @click="seen=!seen;show=!show" v-if="!show" class="bg-red-500 hover:bg-red-300 rounded p-2 text-white my-5">Show Less</button>
    <section v-if="seen">
      <section>
        <h1 class="text-3xl">Les bases</h1>
        <p>Et ceci est un élément qui s'affiche uniquement quand la variable (passée dans la fonction data du composant) est true,<br>
        Vue.js contient plusieurs sélecteurs:
        </p>
        <ul class="list-disc ml-10 mt-5">
          <li>v-if</li>
          <li>v-bind:attr</li>
          <li>v-show</li>
          <li>v-on:event</li>
        </ul>
      </section>
      <section class="mt-10">
        <h1 class="text-3xl">Les formulaires</h1>
        <p>Vue.js supporte également les inputs des formulaires, avec:
        </p>
        <ul class="list-disc ml-10 mt-5">
          <li>v-model</li>
        </ul>
      </section>
      <section class="mt-10">
        <h1 class="text-3xl">Les composants</h1>
        <p>Vue.js fonctionne avec un système de composants.
        </p>
        <img src="../assets/capture1.png">
      </section>
    </section>
  </header>
</template>

<script>
export default {
  name: 'Welcome',
  data() {
    return {
      seen: false,
      show: "Show more"
    }
  },
  props: {
    msg: String,
  }
}
</script>