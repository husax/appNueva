<script>
  import JsxSetup from "./components/JSXSetup.svelte";
  import JsxBoard from "./components/JsxBoard.svelte";

  const boardAttributes= {
    axis: true,
    boundingbox: [-20, 10, 10, -15],
  };

  const jxgCajaId="cajaGraf";

</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<JsxSetup/>
<JsxBoard {jxgCajaId}/>