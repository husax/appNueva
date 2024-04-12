<script>
  import JXG from "../utils/jsxgraphcore.mjs";
  import { onMount, onDestroy } from "svelte";

  export let boardAttributes= {
    axis: true,
    boundingbox: [-10, 1000, 10, -100],
  };

  export let jxgCajaId;

  onMount( () => {
    const board= JXG.JSXGraph.initBoard(jxgCajaId, boardAttributes);
    const f= board.create('functiongraph', ['exp(x**2)+100']);
    const g= board.create('functiongraph', ['x**2+100']);
  });

  onDestroy( () => {
    console.log("Se destruyo el componente JsxGraph");
  })

  console.log("version jsxgraph: ", JXG.version);
</script>

<div id={jxgCajaId} class="jxgbox"></div>

<style>
  div {
    width: 50%;
    height: 40em;
    border: 3px solid green;
  }
</style>