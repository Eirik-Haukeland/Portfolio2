<script>
  export let imgSrc
  export let imgAlt
  export let projectTitle
  export let repoUrl
  export let liveUrl = ''
</script>

<div class="w-72 xl:w-96 h-min p-2 bg-zinc-100 flex flex-col rounded">
  <img src={imgSrc} alt={imgAlt}>
  <h3 class="capitalize text-xl font-bold">{projectTitle}</h3>
  <a href={repoUrl} class="text-blue-500 hover:text-blue-800 focus:text-blue-800">repo for {projectTitle}</a>
  {#if liveUrl !== ''}
    <a href={liveUrl} class="text-blue-500 hover:text-blue-800 focus:text-blue-800">livePage for {projectTitle}</a>
  {/if}
</div>
