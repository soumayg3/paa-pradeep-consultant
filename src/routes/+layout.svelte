<script>
  import '../app.css';
  import Navbar from '$lib/components/Navbar.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  {@html `<script type="application/ld+json">${JSON.stringify({
    "@context": "https://schema.org",
    "@type": "Person",
    "name": "Pradeep Kumar Gupta",
    "jobTitle": "Pulp and Paper Technologist, Quality Consultant and Independent Director Candidate",
    "url": "https://www.pradeepkumargupta.in",
    "image": "https://www.pradeepkumargupta.in/pradeep-kumar-gupta-full.webp",
    "sameAs": ["https://www.linkedin.com/in/pkg9673/"],
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Ghaziabad",
      "addressRegion": "Uttar Pradesh",
      "addressCountry": "IN"
    },
    "alumniOf": {
      "@type": "CollegeOrUniversity",
      "name": "IIT Roorkee"
    },
    "knowsAbout": [
      "Pulp and Paper Technology", "Total Quality Management", "Quality Management Systems",
      "Corporate Governance", "Lean Six Sigma", "ISO Standards", "Operational Excellence",
      "MSME Competitiveness", "Occupational Health and Safety"
    ]
  })}</script>`}
</svelte:head>

<Navbar />
<slot />
<Footer />
