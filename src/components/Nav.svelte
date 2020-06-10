<script>
  export let segment;
</script>

<style>
</style>

<div class="flex justify-between px-10 py-4">
<div class="text-xl font-bold">Marco Monsanto</div>
<nav>
  <ul class="flex">
    <li class="block p-2">
      <a
        aria-current={segment === undefined ? 'page' : undefined}
        href="."
        class="text-lg">
        Home
      </a>
    </li>
    <li class="block p-2">
      <a
        aria-current={segment === 'about' ? 'page' : undefined}
        href="about"
        class="text-lg">
        About
      </a>
    </li>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <li class="block p-2">
      <a
        rel="prefetch"
        aria-current={segment === 'blog' ? 'page' : undefined}
        href="blog"
        class="text-lg">
        Blog
      </a>
    </li>
  </ul>
</nav>
</div>