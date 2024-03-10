<script>
  export let imgSrc
  export let imgAlt
  export let projectTitle
  export let repoUrl
  export let liveUrl = ''
</script>

<div class="w-64 h-min p-2 bg-zinc-50 flex flex-col rounded">
  <img src={imgSrc} alt={imgAlt}>
  <h3>{projectTitle}</h3>
  <a href={repoUrl} class="text-blue-500">link to repo for {projectTitle}</a>
  {#if liveUrl !== ''}
    <a href={liveUrl} class="text-blue-500">link to livePage for {projectTitle}</a>
  {/if}
</div>
