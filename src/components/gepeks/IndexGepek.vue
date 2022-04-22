<template>
<div>
  <ul class="nav">
  <li class="nav-item">
    <a class="nav-link active" aria-current="page" href="#">Főoldal</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Gépek</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Hibajelentések</a>
  </li>
</ul>
<table>
      <thead>
        <tr>
          <th>Épület</th>
          <th>Emelet</th>
          <th>Terem</th>
          <th>Gép</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="statue in statues" v-bind:key="statue.id">
          <td>{{ statue.person }}</td>
          <td>{{ statue.height }}</td>
          <td>{{ statue.price }}</td>
          <td>
            <button @click="deleteStatue(statue.id)">Törlés</button>
            <button @click="editStatue(statue.id)">Szerkesztés</button>
          </td>
        </tr>
      </tbody>
    </table>
</div>
</template>

<script>
export default {
    setup() {
        
    },
}
</script>

<style>

</style>