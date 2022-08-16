<script lang="ts">
  let extraLegs = 1;
  let docPos = 0;

  $: heightDiff = docPos + window.innerHeight;
  $: extraLegs = Math.ceil((heightDiff / 24) + 10);
</script>


<svelte:window bind:scrollY={docPos} />
<main class="w-full" >
  <pre class="mx-auto w-fit"> 
     ,
_,,)\.~,,._
(()`  ``)\))),,_
 |     \ ''((\)))),,_          ____
 |6`   |   ''((\())) "-.____.-"    `-.-,
 |    .'\    ''))))'                  \)))
 |   |   `.     ''                     ((((
 \, _)     \/                          |))))
  `'        |                          (((((
            \                  |       ))))))
             `|    |           ,\     /((((((
              |   / `-.______.&lt;  \   |  )))))
              |   |  /         `. \  \  ((((
              |  / \ |           `.\  | (((
              \  | | |             )| |  ))
               | | | |             || |  '
      	       | | | |             || |  
      	       | | | |             || |  
      	       | | | |             || |  
      	       | | | |             || |  
      	       | | | |             || |  
      	       | | | |             || |  
</pre>
{#each Array(extraLegs) as _ } 
<pre class="mx-auto w-fit">
      	   | | | |             || |  
</pre>
{/each}
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    margin: 0 auto;
  }
</style>
