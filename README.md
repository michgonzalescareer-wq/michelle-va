<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Michelle Gonzales | Administrative & Financial Operations</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto+Slab:wght@400;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<style>
/* --- Reset & Base --- */
* { margin:0; padding:0; box-sizing:border-box; }
body { font-family:'Poppins',sans-serif; background:#0b2a4a; color:white; line-height:1.6; overflow-x: hidden; }
html { scroll-behavior:smooth; }

/* --- Layout Centering Logic --- */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    width: 100%;
}

section { 
    width: 100%;
    padding: 80px 0; 
    opacity:0; 
    transform: translateY(40px); 
    transition: all 0.6s ease; 
}

section.visible { opacity:1; transform: translateY(0); }
h2 { font-family:'Roboto Slab',serif; text-align:center; margin-bottom:40px; color:#7cb9ff; font-size:2rem; }

/* --- NAVIGATION --- */
nav { background:#081f36; position:sticky; top:0; padding:15px; text-align:center; z-index:999; border-bottom:2px solid #1a73e8; width: 100%; }
nav a { color:white; margin:0 12px; text-decoration:none; font-size:0.75rem; font-weight:600; text-transform:uppercase; transition: color 0.3s; }
nav a:hover { color:#1a73e8; }

/* --- HERO SECTION --- */
header { 
    height:70vh; 
    display:flex; 
    flex-direction:column; 
    align-items:center; 
    justify-content:center; 
    text-align:center; 
    background: linear-gradient(rgba(11, 42, 74, 0.88), rgba(11, 42, 74, 0.88)), 
                url("hero/hero_bg.jpg"); 
    background-size:cover; 
    background-position:center; 
    width: 100%;
}
header h1 { font-size:3.5rem; margin-bottom:10px; padding: 0 20px; }
header p { opacity: 0.9; font-size: 1.1rem; padding: 0 20px; }
.hero-buttons { margin-top:25px; display:flex; gap:15px; flex-wrap:wrap; justify-content:center; padding: 0 20px; }
.hero-buttons a { padding:12px 25px; border-radius:40px; text-decoration:none; color:white; font-weight:600; transition: transform 0.3s; display: flex; align-items: center; gap: 8px; }
.hero-buttons a:hover { transform: scale(1.05); }
.linkedin-btn { background:#0A66C2; }
.whatsapp-btn { background:#25D366; }
.book-btn { background:#1a73e8; }

/* --- ABOUT --- */
.about-box { background:white; color:#0b2a4a; border-radius:20px; margin-top:-40px; padding:50px; box-shadow:0 10px 30px rgba(0,0,0,.3); display:flex; flex-wrap:wrap; align-items:center; gap:40px; }
.about-img { width:250px; height:250px; object-fit:cover; border-radius:20px; flex-shrink:0; transition: transform 0.3s; }
.about-img:hover { transform: scale(1.05); }
.about-text { flex:1; }
.about-text h2 { color:#0b2a4a; text-align:left; font-size:2rem; margin-bottom:15px; }
.about-text p { margin-top:10px; }

/* --- PROFESSIONAL ADVANTAGE --- */
#value-inner { background:#15417c; border-radius:20px; padding:60px 40px; text-align:center; width: 100%; }
.prop-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:25px; margin-top:30px; text-align:left; }
.check { display:flex; gap:15px; background: rgba(255,255,255,0.15); padding:15px; border-radius:15px; transition: transform 0.3s; }
.check:hover { transform: translateY(-5px); }
.check i { font-size:1.4rem; color:#25D366; }

/* --- CORE EXPERTISE --- */
.grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:30px; }
.card { background:rgba(255,255,255,0.05); padding:0; border-radius:15px; border:1px solid rgba(255,255,255,0.1); transition: transform 0.3s, background 0.3s; cursor:pointer; text-align:center; overflow:hidden; }
.card:hover { transform: translateY(-10px); background: rgba(255,255,255,0.1); }
.card img { width:100%; height:200px; object-fit:cover; display:block; margin-bottom:20px; }
.card h3 { padding: 0 15px; margin-bottom:10px; }
.card p { padding: 0 15px 25px 15px; font-size: 0.9rem; }

/* --- PORTFOLIO --- */
.portfolio-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(300px,1fr)); gap:25px; }

/* Existing Portfolio Item Styles */
.portfolio-item { background:white; border-radius:15px; overflow:hidden; color:#0b2a4a; box-shadow:0 10px 20px rgba(0,0,0,0.2); transition: transform 0.3s; }
.portfolio-item:hover { transform: scale(1.02); }
.portfolio-img-container { width:100%; height:220px; background:#f0f0f0; display:flex; align-items:center; justify-content:center; position:relative; overflow:hidden; border-bottom:1px solid #ddd; }
.portfolio-img-container img { width:100%; height:100%; object-fit:cover; }
.portfolio-info { padding:20px; }
.portfolio-info h3 { font-size:1.2rem; margin-bottom:8px; color:#1a73e8; }
.portfolio-tag { display:inline-block; background:#e1efff; color:#1a73e8; font-size:0.75rem; padding:3px 10px; border-radius:20px; font-weight:600; margin-bottom:10px; }

/* --- WORKFLOW --- */
.flow { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; }
.flow-card { background:rgba(26,115,232,.1); padding:30px; border-radius:15px; border-top:4px solid #1a73e8; position:relative; transition: transform 0.3s; cursor:pointer; }
.flow-card:hover { transform: translateY(-5px); }
.step { position:absolute; top:-15px; left:20px; background:#1a73e8; width:35px; height:35px; border-radius:50%; display:flex; align-items:center; justify-content:center; font-weight:bold; color:white; }

/* --- TOOLS --- */
.tools { display:grid; grid-template-columns:repeat(auto-fit,minmax(130px,1fr)); gap:15px; }
.tool { background:white; color:#0b2a4a; text-align:center; padding:20px; border-radius:12px; transition: transform 0.3s; cursor:pointer; }
.tool:hover { transform: translateY(-5px); }
.tool img { height:40px; margin-bottom:8px; }

/* --- CERTIFICATIONS --- */
#cert-inner { background: rgba(255,255,255,0.05); border-radius: 20px; padding: 60px 40px; width: 100%; }
.cert-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; }
.cert-card { background: white; color: #0b2a4a; padding: 15px; border-radius: 12px; text-align: center; box-shadow: 0 4px 15px rgba(0,0,0,0.1); transition: transform 0.3s; display: flex; flex-direction: column; justify-content: space-between; }
.cert-card:hover { transform: translateY(-5px); }
.cert-card img { width: 100%; height: 140px; object-fit: contain; margin-bottom: 10px; border-radius: 8px; border: 1px solid #eee; }
.cert-card h3 { font-size: 0.85rem; color: #1a73e8; line-height: 1.2; font-weight: 600; }
.cert-card p { font-size: 0.75rem; margin-top: 5px; opacity: 0.7; }

/* --- FAQ --- */
.faq-container { max-width:800px; margin:auto; }
.faq-item { background:white; color:#0b2a4a; margin-bottom:15px; border-radius:10px; overflow:hidden; cursor:pointer; }
.faq-question { padding:20px; font-weight:600; display:flex; justify-content:space-between; align-items:center; }
.faq-answer { max-height:0; overflow:hidden; padding:0 20px; transition: max-height 0.3s ease, padding 0.3s ease; }
.faq-item.active .faq-answer { max-height:1000px; padding:20px; }
.faq-question i { transition: transform 0.3s; }
.faq-item.active .faq-question i { transform: rotate(180deg); }

/* --- CTA & CONTACT --- */
.cta-wrapper { width: 100%; padding: 80px 20px; }
.cta-box { background: linear-gradient(135deg, #1a73e8 0%, #0b2a4a 100%); padding: 100px 40px; border-radius: 30px; text-align: center; position: relative; overflow: hidden; box-shadow: 0 20px 40px rgba(0,0,0,0.4); max-width: 1200px; margin: 0 auto; }
.cta-box h2 { color: white; font-size: 2.5rem; margin-bottom: 15px; }
.cta-box p { font-size: 1.1rem; margin-bottom: 35px; opacity: 0.9; max-width: 600px; margin-left: auto; margin-right: auto; }
.btn-cta { background: #25D366; color: white; padding: 18px 45px; border-radius: 50px; text-decoration: none; font-weight: 700; font-size: 1.2rem; display: inline-flex; align-items: center; gap: 10px; transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275); box-shadow: 0 10px 20px rgba(37, 211, 102, 0.3); }
.btn-cta:hover { transform: scale(1.1) translateY(-3px); background: #20ba5a; }
.cta-contact-grid { display: flex; justify-content: center; gap: 50px; margin-top: 50px; padding-top: 30px; border-top: 1px solid rgba(255, 255, 255, 0.2); flex-wrap: wrap; }
.cta-contact-item { color: white; text-decoration: none; font-size: 1rem; display: flex; align-items: center; gap: 12px; transition: all 0.3s ease; padding: 10px 15px; }
.cta-contact-item:hover { opacity: 0.8; transform: translateY(-2px); }
.cta-contact-item i { color: #7cb9ff; font-size: 1.2rem; }

/* --- FLOATING WHATSAPP --- */
.whatsapp-float { position: fixed; bottom:25px; right:25px; background:#25D366; color:white; font-size:26px; padding:15px 18px; border-radius:50%; box-shadow:0 6px 15px rgba(0,0,0,0.3); z-index:999; display:flex; align-items:center; justify-content:center; text-decoration:none; transition: transform 0.3s; }
.whatsapp-float:hover { transform: scale(1.1); }

/* --- RESPONSIVE --- */
@media (max-width: 1024px) {
    .cert-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 768px) {
    .about-box { padding: 30px; flex-direction: column; text-align: center; }
    .about-text h2 { text-align: center; }
    header h1 { font-size: 2.5rem; }
}
@media (max-width: 600px) {
    .cta-contact-grid { flex-direction: column; gap: 20px; }
    header h1 { font-size: 2.2rem; }
    .cert-grid { grid-template-columns: 1fr; }
}
</style>
</head>

<body>

<nav>
    <a href="#about">Profile</a>
    <a href="#services">Expertise</a>
    <a href="#portfolio">Sample Works</a>
    <a href="#workflow">Workflow</a>
    <a href="#tools">Tools</a>
    <a href="#certifications">Certifications</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</nav>

<header>
    <h1>Michelle Gonzales</h1>
    <p>Administrative • Accounts Receivable • Bookkeeping • Payroll Support</p>
    <div class="hero-buttons">
        <a href="https://www.linkedin.com/in/michgonzalesva" target="_blank" class="linkedin-btn"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="https://wa.me/639654033089" target="_blank" class="whatsapp-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
        <a href="https://cal.com/michgonzalesva" target="_blank" class="book-btn"><i class="fas fa-calendar"></i> Book Discovery Call</a>
    </div>
</header>

<section id="about">
    <div class="container">
        <div class="about-box">
            <img src="gonzales/Gonzales_Michelle.jpg" class="about-img" alt="Michelle Gonzales">
            <div class="about-text">
                <h2>Operational Partner</h2>
                <p>I specialize in streamlining back-office operations and financial documentation. While I have a strong command of accounting fundamentals, I am currently onboarding QuickBooks into my service suite to provide clients with modern, cloud-based reporting and real-time financial tracking.</p>
            </div>
        </div>
    </div>
</section>

<section id="value">
    <div class="container">
        <div id="value-inner">
            <h2>Professional Advantage</h2>
            <div class="prop-grid">
                <div class="check"><i class="fas fa-check-circle"></i><div><h3>Corporate Discipline</h3><p>Structured documentation and organized records.</p></div></div>
                <div class="check"><i class="fas fa-check-circle"></i><div><h3>Process Organization</h3><p>Reliable workflows for business operations.</p></div></div>
                <div class="check"><i class="fas fa-check-circle"></i><div><h3>Reliable Communication</h3><p>Professional support across teams.</p></div></div>
            </div>
        </div>
    </div>
</section>

<section id="services">
    <div class="container">
        <h2>Core Expertise</h2>
        <div class="grid">
            <div class="card"><img src="expertise/admin.jpg" alt="Executive Admin"><h3>Executive Administration</h3><p>Email organization, scheduling, document management.</p></div>
            <div class="card"><img src="expertise/bookkeeping.jpg" alt="Bookkeeping"><h3>Bookkeeping Support</h3><p>Transaction documentation and financial record organization. (Learning QuickBooks)</p></div>
            <div class="card"><img src="expertise/ar.jpg" alt="Accounts Receivable"><h3>Accounts Receivable</h3><p>Invoice tracking and payment monitoring.</p></div>
            <div class="card"><img src="expertise/payroll.jpg" alt="Payroll"><h3>Payroll Documentation</h3><p>Organizing payroll records and salary tracking.</p></div>
        </div>
    </div>
</section>

<!-- --- PORTFOLIO WITH 5 ITEMS --- -->
<section id="portfolio">
    <div class="container">
        <h2>Sample Works & Reports</h2>
        <div class="portfolio-grid">

            <!-- Profit & Loss -->
            <div class="portfolio-item">
                <div class="portfolio-img-container">
                    <img src="qbo/profitandloss.jpg" alt="Profit & Loss Statement">
                </div>
                <div class="portfolio-info">
                    <span class="portfolio-tag">QuickBooks Online</span>
                    <h3>Profit & Loss Statement</h3>
                    <p>Mock monthly Profit & Loss report showing income, expenses, and net profit for a sample business.</
