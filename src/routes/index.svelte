<script>
  import Button from "@smui/button";
  import Fab from "@smui/fab";
  import Textfield from "@smui/textfield";
  import HelperText from "@smui/textfield/helper-text";
  import { Label, Icon } from "@smui/common";

  let superText = "";
</script>

<style>
  h1,
  figure,
  p {
    text-align: center;
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  figure {
    margin: 0 0 1em 0;
  }

  img {
    width: 100%;
    max-width: 400px;
    margin: 0 0 1em 0;
  }

  p {
    margin: 1em auto;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
</style>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>

<h1>Great success!</h1>

<Button on:click={() => alert('Clicked!')}>Just a Button</Button>
<Button variant="raised">
  <Label>Raised Button, Using a Label</Label>
</Button>
<Button some-arbitrary-prop="placed on the actual button">Button</Button>

<Fab on:click={() => alert('Clicked!')} extended>
  <Icon class="material-icons" style="margin-right: 12px;">favorite</Icon>
  <Label>Extended FAB</Label>
</Fab>

<Textfield
  bind:value={superText}
  label="Super Text"
  input$aria-controls="super-helper"
  input$aria-describedby="super-helper" />
<HelperText id="super-helper">
  What you put in this box will become super!
</HelperText>

<figure>
  <img alt="Borat" src="great-success.png" />
  <figcaption>HIGH FIVE!</figcaption>
</figure>

<p>
  <strong>
    Try editing this file (src/routes/index.svelte) to test live reloading.
  </strong>
</p>
