<script setup lang="ts">

</script>

<template>
  <h2>Test</h2>

  <button class="btn">Suivant</button>

 


</template>

<style scoped lang="css">

.btn{ 
  padding:1rem;
  background:rgba(81, 81, 240,1);
  font-size:1.2rem;
  border-radius:5px;
  border:none;
  cursor: pointer;

}
.btn:hover{ 
  transition: all .5s ease-in-out;
background:rgba(81, 81, 240,.7);
}
h2 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
  color:crimson;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
