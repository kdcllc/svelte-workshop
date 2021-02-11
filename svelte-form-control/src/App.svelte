<script>
  import Textfield from "@smui/textfield";
  import Card, {
    Content,
    PrimaryAction,
    Media,
    MediaContent,
    Actions,
    ActionButtons,
    ActionIcons,
  } from "@smui/card";
  import Button, { Label } from "@smui/button";
  import IconButton, { Icon } from "@smui/icon-button";
  import List, { Item, Text } from "@smui/list";

  import { onMount, onDestroy } from "svelte";
  import TestForm from "./TestForm.svelte";
  export let name;

  let d = "";
  let clicked = 0;

  $: console.log(d);
  $: console.log(clicked);

  function handleRedirect() {
    window.location = "https://svelte.dev/tutorial";
  }
</script>

<main>
  <div class="container">
    <!-- <div class="row columns margins">
      <Textfield
        bind:value={d}
        label="Date"
        type="date"
        defaultValue={new Date()}
      />
    </div> -->

    <div class="row card-container short">
	<Card>
		<Content>Hello {name}!</Content>
		<Actions fullBleed>
		  <Button on:click={handleRedirect}>
			<Label>Svelte tutorial</Label>
			<i class="material-icons" aria-hidden="true">arrow_forward</i>
		  </Button>
		</Actions>
	</Card>

    </div>
  </div>
  <div class="row">
	  <Card>
		<TestForm />
	  </Card>
  </div>
</main>

<style>
  .margins {
    margin: 18px 0 24px;
  }
  .card-container {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    min-height: 500px;
    min-width: 380px;
    background-color: #f8f8f8;
    margin-right: 20px;
    margin-bottom: 20px;
  }
  .card-container.short {
    min-height: 200px;
  }

  * :global(.card-media-16x9) {
    background-image: url(https://via.placeholder.com/320x180.png?text=16x9);
  }

  * :global(.card-media-square) {
    background-image: url(https://via.placeholder.com/320x320.png?text=square);
  }
</style>
