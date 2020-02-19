<script>
  import Tags from "../components/Tags.svelte";
  import posts from "../posts.js";

  let filterTerm = "fiction";

  const updateFilterTerm = term => {
    filterTerm = term;
  };

  $: filteredStories = posts.stories.filter(story =>
    story.tags.includes(filterTerm)
  );
</script>

<style>
  p {
    color: white;
  }
</style>

<Tags tags={posts.tags.split(',')} />

{#each filteredStories as story}
  <p>{story.title}</p>
{/each}
