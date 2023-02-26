<script>
  const url = window.location.pathname;

  const listLinks = [
  { name: "Inicio", path: "/" },
  { name: "Las Fibras", path: "/las-fibras" },
  { name: "Comunidad", path: "/comunidad" },
  { name: "Blog", path: "/blog" },
];
</script>

<nav class="nav">
  <div class="logo">
    <a href="/">Fibras MX</a>
  </div>

  <ul class="nav__links">
    {#each listLinks as link}
      <li class="nav__link" > 
        <a class={link.path === url ? 'link active' : 'link'} href={link.path}>{link.name}</a>
      </li> 
    {/each}
  </ul>
</nav>
