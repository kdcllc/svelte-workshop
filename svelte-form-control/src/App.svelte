<script>
  import { onMount, onDestroy  } from "svelte";
  export let name;

  let picker;

  let d = '';

  onMount(async () => {
	var elem = document.querySelectorAll('.datepicker');
    picker = M.Datepicker.getInstance(elem[0]);
	d = picker.toString();
  });

  onDestroy(() => {
		picker.destroy();
	});

  function handleDateChange(event) {
    d = event.target.value;
  }

  $: console.log(picker)
</script>

<main>

  <div class="container">
    <div class="row">
      <input type="text" on:change={handleDateChange} class="datepicker" />
    </div>
    <div class="row">
      <div class="col s12 m6">
        <div class="card blue-grey darken-1">
          <div class="card-content white-text">
            <span class="card-title">Welcome</span>
            <p>Hello {name}!</p>
            <p>{d}</p>
          </div>
          <div class="card-action">
            <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
          </div>
        </div>
      </div>
    </div>
    <div />
  </div>
</main>
