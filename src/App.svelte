<script>
  import Tarjeta from "./Tarjeta.svelte";
  let AzulPoints=20;
  let RojoPoints=20;

  function resetPoints(){
    AzulPoints=20;
    RojoPoints=20;
  }
</script>




<Tarjeta name="Azul" bind:points={AzulPoints} style="primary"/>
<Tarjeta name="Rojo" bind:points={RojoPoints} style="secondary"/>
{#if AzulPoints<=0}
<h3>Rojo Gana</h3>
{:else if RojoPoints<=0}
<h3>Azul Gana</h3>
{:else}
<h3>Nadie gana aún</h3>
{/if}
<button type="reset" on:click={resetPoints}>Reset</button>
