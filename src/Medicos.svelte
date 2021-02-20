<script>
  import { onMount, getContext } from "svelte";
  import { jsonData }            from "./store.js";

  import Buscar                  from "./Buscar.svelte";
  import Medico                from "./Medico.svelte";
  import Boton                   from "./Boton.svelte";

  const URL = getContext("URL");

  let busqueda = "";
  let medico = {};

  onMount(async () => {
    const response = await fetch(URL.medicos);
    const data = await response.json();
    $jsonData = data;
  });

  $: regex = new RegExp(busqueda, "i");
  $: datos = busqueda 
    ? $jsonData.filter(item => regex.test(item.nombre))
    : $jsonData;

</script>

<style>
  .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: left;
    flex-wrap: wrap;
  }
</style>

<h1>MEDICOS</h1>
<Buscar bind:busqueda />

<div class="container">
  <Medico bind:medico>
    <div style="text-align: right">
      <Boton documento={medico} tipo="insertar" coleccion="medicos" />
    </div>
  </Medico>
</div>

<div class="container">
  {#each datos as medico}
    <Medico {medico}>
      <div style="text-align: right">
        <Boton documento={medico} tipo="modificar" coleccion="medicos" />
        <Boton documento={medico} tipo="eliminar"  coleccion="medicos" />
      </div>
    </Medico>
  {/each}
</div>
