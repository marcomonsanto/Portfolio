<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`blog.json`)
      .then(r => r.json())
      .then(posts => {
				console.log('posts: ', posts)
        return { posts };
      });
  }
</script>

<script>
  export let posts;
</script>

<style>
</style>

<svelte:head>
  <title>Blog</title>
</svelte:head>

<h1 class="text-6xl">Recent posts</h1>

{#each posts as post}
  <!-- we're using the non-standard `rel=prefetch` attribute to
			tell Sapper to load the data for the page as soon as
			the user hovers over the link or taps it, instead of
			waiting for the 'click' event -->
  <a rel="prefetch" href="blog/{post.slug}">
    <article class="max-w-sm border rounded border-gray-200">
      {post.title}
    </article>
  </a>
{/each}
