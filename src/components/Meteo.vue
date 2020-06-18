<template>
  <div class="container">
    <h1 class="my-4">App Météo avec VueJS</h1>

    <div class="form-group mb-5">
      <label for="position">Entrez le nom d'une ville</label>
      <input
        id="position"
        type="text"
        class="form-control"
        v-model="requete"
        v-on:keypress="goMeteo"
      />
    </div>
    <div class="w-75 m-auto">
      <h3 class="text-center mb-3">Position: Paris</h3>
      <div class="card text-center p-5">
        <p class="text-affichage">Temperature: 20°</p>
        <p class="texte-affichage">Temps : Nuageux</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Meteo',
  data() {
    return {
      requete: '',
      temps: undefined,
      api_code: '9f296d1ca18093e4dc31d6ade8221ce1',
      url_recherche: 'api.openweathermap.org/data/2.5/weather?',
    };
  },
};
</script>

<style></style>
