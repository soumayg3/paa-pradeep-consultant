<script>
  import { onMount } from 'svelte';
  import { page } from '$app/stores';

  let scrolled = false;
  let menuOpen = false;

  onMount(() => {
    const handler = () => { scrolled = window.scrollY > 40; };
    window.addEventListener('scroll', handler, { passive: true });
    return () => window.removeEventListener('scroll', handler);
  });

  function closeMenu() { menuOpen = false; }

  const navLinks = [
    { label: 'Home',    href: '/' },
    { label: 'Work',    href: '/work' },
    { label: 'About',   href: '/about' },
    { label: 'Contact', href: '/contact' },
  ];

  function isActive(href, pathname) {
    if (href === '/') return pathname === '/';
    return pathname.startsWith(href);
  }
</script>

<nav class:scrolled>
  <div class="container nav-inner">
    <a href="/" class="logo" on:click={closeMenu}>
      <span class="logo-mark">PKG</span>
      <span class="logo-text">Pradeep Kumar Gupta</span>
    </a>

    <button
      class="burger"
      aria-label="Toggle menu"
      aria-expanded={menuOpen}
      on:click={() => menuOpen = !menuOpen}
    >
      <span></span><span></span><span></span>
    </button>

    <ul class="nav-links" class:open={menuOpen}>
      {#each navLinks as { label, href }}
        <li>
          <a
            {href}
            class:active={isActive(href, $page.url.pathname)}
            on:click={closeMenu}
          >{label}</a>
        </li>
      {/each}
      <li>
        <a href="https://wa.me/917669697397" class="nav-cta" target="_blank" rel="noopener">
          WhatsApp
        </a>
      </li>
    </ul>
  </div>
</nav>

<style>
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  padding: 1.4rem 0;
  background: rgba(242,246,251,0.85);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid transparent;
  transition: background 0.35s, padding 0.35s, box-shadow 0.35s, border-color 0.35s;
}
nav.scrolled {
  background: rgba(242,246,251,0.97);
  padding: 0.85rem 0;
  box-shadow: 0 4px 20px rgba(20,97,164,0.08);
  border-color: var(--border);
}

.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  color: var(--navy);
}
.logo-mark {
  font-family: var(--font-display);
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--logo-gold);
  letter-spacing: 0.05em;
}
.logo-text {
  font-family: var(--font-body);
  font-size: 0.78rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 2.5rem;
  list-style: none;
}
.nav-links a {
  font-size: 0.75rem;
  font-weight: 400;
  letter-spacing: 0.13em;
  text-transform: uppercase;
  color: var(--muted);
  transition: color 0.2s;
  position: relative;
}
.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -4px; left: 0; right: 0;
  height: 1px;
  background: var(--accent);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.25s ease;
}
.nav-links a:hover,
.nav-links a.active { color: var(--navy); }
.nav-links a:hover::after,
.nav-links a.active::after { transform: scaleX(1); }

.nav-cta {
  background: var(--accent) !important;
  color: #fff !important;
  padding: 0.55em 1.4em;
  border-radius: 2px;
  font-weight: 500 !important;
  transition: background 0.2s, transform 0.2s !important;
}
.nav-cta:hover {
  background: var(--accent-light) !important;
  transform: translateY(-1px) !important;
}
.nav-cta::after { display: none !important; }

/* burger */
.burger {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px;
}
.burger span {
  display: block;
  width: 24px;
  height: 2px;
  background: var(--navy);
  transition: transform 0.25s, opacity 0.25s;
}

@media (max-width: 768px) {
  .burger { display: flex; }
  .nav-links {
    position: fixed;
    top: 0; right: -100%;
    width: 75vw;
    max-width: 300px;
    height: 100vh;
    background: var(--navy);
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    gap: 2rem;
    padding: 2rem;
    transition: right 0.35s ease;
  }
  .nav-links.open { right: 0; box-shadow: -8px 0 40px rgba(0,0,0,0.4); }
  .nav-links a { font-size: 1rem; }
}
</style>
