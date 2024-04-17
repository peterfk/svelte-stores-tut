<script>
  import { count } from "./stores.js";
  import { time } from "./stores.js";
  import Incrementer from "./lib/Incrementer.svelte";
  import Decrementer from "./lib/Decrementer.svelte";
  import Resetter from "./lib/Resetter.svelte";

  const formatter = new Intl.DateTimeFormat("en", {
    hour12: true,
    hour: "numeric",
    minute: "2-digit",
    second: "2-digit",
  });
</script>

<h1>The count is {$count}</h1>

<Incrementer />
<Decrementer />
<Resetter />

<h1>The time is {formatter.format($time)}</h1>