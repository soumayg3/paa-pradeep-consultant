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
    "jobTitle": "Business Consultant & Strategic Advisor",
    "url": "https://www.pradeepkumargupta.in",
    "image": "https://www.pradeepkumargupta.in/image.jpeg",
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
      "Quality Management", "ESG & Sustainability", "Corporate Governance",
      "Lean Six Sigma", "ISO Standards", "Operational Excellence", "CSR"
    ]
  })}</script>`}
</svelte:head>

<Navbar />
<slot />
<Footer />
