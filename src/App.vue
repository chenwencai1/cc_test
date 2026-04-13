<script setup>
const navItems = [
  { label: 'HOME', href: '#home' },
  { label: 'ABOUT US', href: '#about' },
  { label: 'PRODUCTS', href: '#products' },
  { label: 'CERTIFICATE', href: '#certificate' },
  { label: 'NEWS', href: '#news' },
  { label: 'CONTACT US', href: '#contact' },
]

const products = [
  { name: 'Tirz', tag: 'Weight Management', price: '$ 0.00' },
  { name: 'Tesam', tag: 'Hormone Support', price: '$ 0.00' },
  { name: 'SS-31', tag: 'Cellular Energy', price: '$ 0.00' },
  { name: 'Sema', tag: 'Metabolic Research', price: '$ 0.00' },
  { name: 'Reta', tag: 'Clinical Development', price: '$ 0.00' },
  { name: 'NAD+', tag: 'Longevity Formula', price: '$ 0.00' },
  { name: 'KPV-10', tag: 'Peptide Innovation', price: '$ 0.00' },
  { name: 'Ipamorelin', tag: 'Lab Grade', price: '$ 0.00' },
]

const certificates = [
  'ISO 9001 Quality Management',
  'National High-Tech Enterprise',
  'Henan Specialized SME',
  'Patent Achievement Award',
  'Export Compliance Certificate',
  'Bio Safety Standard',
]

const newsItems = [
  {
    title: 'What are the benefits and functions of beauty peptides',
    summary:
      'Anti-aging, anti-oxidation, repair, and anti-edema functions make beauty peptides one of the core tracks in modern formula design.',
    date: '2026-03-19',
  },
  {
    title: 'The beauty benefits and functions of peptides',
    summary:
      'From precision anti-aging plans to skin renewal routines, peptides are becoming a key component in high-performance cosmetic research.',
    date: '2026-03-11',
  },
  {
    title: 'Simple understanding of peptides',
    summary:
      'Peptides bind with cell receptors and participate in signaling pathways, helping regulate secretion and supporting balanced metabolism.',
    date: '2026-03-05',
  },
]
</script>

<template>
  <div class="site">
    <header class="topbar" id="home">
      <div class="brand">
        <span class="brand-mark">M</span>
        <div>
          <p class="brand-name">Mokemei Peptide</p>
          <p class="brand-sub">R&D / Production / Sales</p>
        </div>
      </div>
      <nav class="nav">
        <a v-for="item in navItems" :key="item.label" :href="item.href">{{ item.label }}</a>
      </nav>
    </header>

    <section class="hero">
      <p class="hero-kicker">Recognized Excellence</p>
      <h1>Advanced Peptide Solutions For Health and Beauty</h1>
      <p class="hero-copy">
        Mokemei is mainly engaged in peptide research and manufacturing, with more than 20 years of
        exploration in weight loss peptides and beauty peptides.
      </p>
      <div class="hero-actions">
        <a href="#products" class="btn btn-primary">Explore Products</a>
        <a href="#contact" class="btn btn-ghost">Contact Team</a>
      </div>
    </section>

    <section class="section" id="certificate">
      <div class="section-head">
        <h2>CERTIFICATE</h2>
        <a href="#" class="view-link">View More</a>
      </div>
      <div class="certificate-grid">
        <article v-for="item in certificates" :key="item" class="certificate-card">
          <p>{{ item }}</p>
        </article>
      </div>
    </section>

    <section class="section" id="products">
      <div class="section-head">
        <h2>HOT PRODUCTS</h2>
        <a href="#" class="view-link">View More</a>
      </div>
      <p class="section-intro">
        Mokemei has dozens of patented technologies and peripheral R&D products in the fields of
        weight loss peptides and beauty peptides.
      </p>
      <div class="product-grid">
        <article v-for="item in products" :key="item.name" class="product-card">
          <div class="product-image">{{ item.name.slice(0, 2).toUpperCase() }}</div>
          <p class="product-tag">{{ item.tag }}</p>
          <h3>{{ item.name }}</h3>
          <p class="price">{{ item.price }}</p>
        </article>
      </div>
    </section>

    <section class="section about" id="about">
      <div>
        <h2>ABOUT US</h2>
        <p>
          Mokomei Peptide Co., Ltd is located in Zhengzhou, China. The company integrates scientific
          research and development, production, sales, and technical services.
        </p>
        <p>
          In 2017, it was recognized as a national high-tech enterprise, and in 2021, it was selected
          as a specialized and refined small giant enterprise in Henan Province.
        </p>
      </div>
      <ul class="about-metrics">
        <li>
          <strong>20+</strong>
          <span>Years of peptide exploration</span>
        </li>
        <li>
          <strong>30+</strong>
          <span>Patented technologies</span>
        </li>
        <li>
          <strong>9-17:30</strong>
          <span>Support from Monday to Friday</span>
        </li>
      </ul>
    </section>

    <section class="section" id="news">
      <div class="section-head">
        <h2>NEWS</h2>
        <a href="#" class="view-link">View More</a>
      </div>
      <div class="news-grid">
        <article class="news-card" v-for="item in newsItems" :key="item.title">
          <p class="news-date">{{ item.date }}</p>
          <h3>{{ item.title }}</h3>
          <p>{{ item.summary }}</p>
        </article>
      </div>
    </section>

    <footer class="footer" id="contact">
      <div>
        <p class="footer-title">Contact</p>
        <p>WhatsApp: 86 15132971817</p>
        <p>Email: admin@mokemei.com</p>
        <p>Web: www.mkm-chem.com</p>
      </div>
      <div>
        <p class="footer-title">Address</p>
        <p>
          No. 276 Pengcheng Avenue, Jiulong Office, Zhengzhou Economic and Technological Development
          Zone, China.
        </p>
      </div>
      <div>
        <p class="footer-title">Copyright</p>
        <p>Copyright(C) 20018-2025 All Right Reserved. Mokomei Peptide Co., Ltd</p>
      </div>
    </footer>
  </div>
</template>
