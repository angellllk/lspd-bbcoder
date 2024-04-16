<script setup>
</script>

<template>
  <main>
    <div class="content">
      <p>Acest site contine mai multe pagini care vor genera formate de BBCode precompletate cu datele pe care le puneti la dispozitie. Vezi lista de formate momentan disponibile, alege formatul care te intereseaza, completeaza datele formularuilui si BBCode-ul formatului va fi generat ca atare, gata de postat pe forums. 
      <br><br>
      <b><span style="color: red">(!)</span></b> Nu vezi un format anume? Pentru actualizarea formatelor, vorbiti cu un Command Officer.</p>
      <ul>
        <li><RouterLink to="/dor">DOR</RouterLink></li>
      </ul>
    </div>
    
  </main>
</template>

<style>
.content {
  width: 75vw;
}

li {
  font-size: 24px;
}

.content {
  margin-top: 1rem;
}

p {
  font-size: 24px;
  display: block;
}
</style>
