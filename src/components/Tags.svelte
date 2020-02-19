<script>
  export let tags;
</script>

<style>
  tag {
    color: blue;
  }
</style>

{#each tags as tag}
  <tag>{tag}</tag>
{/each}
