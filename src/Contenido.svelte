<script>
  import { Route }  from "svelte-routing";
  import Inicio     from "./Inicio.svelte";
  import Medicos  from "./Medicos.svelte";
  import Pacientes   from "./Pacientes.svelte";
</script>

<style>
  main {
    padding: 20px;
    padding-top: 50px;
  }
</style>

<main id="contenido">
  <Route path="/" component={Inicio} />
  <Route path="/medicos" component={Medicos} />
  <Route path="/pacientes" component={Pacientes} />
</main>
