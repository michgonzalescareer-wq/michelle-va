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
body { font-family:'Poppins',sans-serif; background:#0b2a4a; color:white; line-height:1.6; }
html { scroll-behavior:smooth; }
section { max-width:1200px; margin:auto; padding:80px 20px; opacity:0; transform: translateY(40px); transition: all 0.6s ease; }
section.visible { opacity:1; transform: translateY(0); }
h2 { font-family:'Roboto Slab',serif; text-align:center; margin-bottom:40px; color:#7cb9ff; font-size:2rem; }

/* --- NAVIGATION --- */
nav { background:#081f36; position:sticky; top:0; padding:15px; text-align:center; z-index:999; border-bottom:2px solid #1a73e8; }
nav a { color:white; margin:0 12px; text-decoration:none; font-size:0.75rem; font-weight:600; text-transform:uppercase; transition: color 0.3s; }
nav a:hover { color:#1a73e8; }

/* --- HERO --- */
header { height:60vh; display:flex; flex-direction:column; align-items:center; justify-content:center; text-align:center; background: linear-gradient(rgba(11,42,74,0.85),rgba(11,42,74,0.85)), url("https://images.unsplash.com/photo-1497215728101-856f4ea42174?w=1600"); background-size:cover; background-position:center; }
header h1 { font-size:3rem; margin-bottom:10px; }
header p { opacity:.9; }
.hero-buttons { margin-top:25px; display:flex; gap:15px; flex-wrap:wrap; justify-content:center; }
.hero-buttons a { padding:12px 22px; border-radius:40px; text-decoration:none; color:white; font-weight:600; transition: transform 0.3s; }
.hero-buttons a:hover { transform: scale(1.05); }
.linkedin-btn { background:#0A66C2; }
.whatsapp-btn { background:#25D366; }
.book-btn { background:#1a73e8; }

/* --- ABOUT / OPERATIONAL PARTNER --- */
#about { background:white; color:#0b2a4a; border-radius:20px; margin-top:-40px; padding:50px; box-shadow:0 10px 30px rgba(0,0,0,.3); display:flex; flex-wrap:wrap; align-items:center; gap:40px; }
.about-img { width:250px; height:250px; object-fit:cover; border-radius:20px; flex-shrink:0; transition: transform 0.3s; }
.about-img:hover { transform: scale(1.05); }
.about-text { flex:1; }
.about-text h2 { color:#0b2a4a; text-align:left; font-size:2rem; margin-bottom:15px; }
.about-text p { margin-top:10px; }

/* --- PROFESSIONAL ADVANTAGE --- */
#value { background:#1a73e8; border-radius:20px; padding:60px 40px; text-align:center; }
.prop-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:25px; margin-top:30px; text-align:left; }
.check { display:flex; gap:15px; background: rgba(255,255,255,0.1); padding:15px; border-radius:15px; transition: transform 0.3s; }
.check:hover { transform: translateY(-5px); }
.check i { font-size:1.4rem; color:#25D366; }

/* --- CORE EXPERTISE CARDS --- */
.grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; }
.card { background:rgba(255,255,255,0.05); padding:25px; border-radius:15px; border:1px solid rgba(255,255,255,0.1); transition: transform 0.3s, background 0.3s; cursor:pointer; }
.card:hover { transform: translateY(-5px); background: rgba(255,255,255,0.1); }
.card i { font-size:2rem; color:#1a73e8; margin-bottom:12px; display:block; }

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
.certs { display:grid; grid-template-columns:repeat(auto-fit,minmax(160px,1fr)); gap:15px; }
.cert { background:white; color:#0b2a4a; padding:10px; border-radius:12px; text-align:center; transition: transform 0.3s; cursor:pointer; }
.cert:hover { transform: translateY(-5px); }
.cert img { width:100%; height:90px; object-fit:contain; margin-bottom:8px; }

/* --- FAQ --- */
.faq { max-width:800px; margin:auto; }
.faq-item { background:white; color:#0b2a4a; margin-bottom:15px; border-radius:10px; overflow:hidden; cursor:pointer; }
.faq-question { padding:20px; font-weight:600; display:flex; justify-content:space-between; align-items:center; }
.faq-answer { max-height:0; overflow:hidden; padding:0 20px; transition: max-height 0.3s ease, padding 0.3s ease; }
.faq-item.active .faq-answer { max-height:1000px; padding:20px; }
.faq-question i { transition: transform 0.3s; }
.faq-item.active .faq-question i { transform: rotate(180deg); }

/* --- CALL TO ACTION --- */
.cta { background:#1a73e8; padding:60px; border-radius:20px; text-align:center; }
.btn { background:white; color:#1a73e8; padding:15px 30px; border-radius:50px; text-decoration:none; font-weight:700; display:inline-block; margin-top:20px; transition: transform 0.3s; }
.btn:hover { transform: scale(1.05); }

/* --- FLOATING WHATSAPP --- */
.whatsapp-float { position:fixed; bottom:25px; right:25px; background:#25D366; color:white; font-size:26px; padding:15px 18px; border-radius:50%; box-shadow:0 6px 15px rgba(0,0,0,0.3); z-index:999; transition: transform 0.3s; }
.whatsapp-float:hover { transform: scale(1.1); }

</style>
</head>

<body>

<!-- NAV -->
<nav>
  <a href="#about">Profile</a>
  <a href="#value">Advantage</a>
  <a href="#services">Expertise</a>
  <a href="#workflow">Workflow</a>
  <a href="#tools">Tools</a>
  <a href="#certs">Certifications</a>
  <a href="#faq">FAQ</a>
  <a href="https://www.linkedin.com/in/michgonzalesva" target="_blank">LinkedIn</a>
</nav>

<!-- HERO -->
<header>
  <h1>Michelle Gonzales</h1>
  <p>Administrative • Accounts Receivable • Bookkeeping • Payroll Support</p>
  <div class="hero-buttons">
    <a href="https://www.linkedin.com/in/michgonzalesva" target="_blank" class="linkedin-btn"><i class="fab fa-linkedin"></i> LinkedIn</a>
    <a href="https://wa.me/639654033089" target="_blank" class="whatsapp-btn"><i class="fab fa-whatsapp"></i> WhatsApp</a>
    <a href="https://cal.com/michgonzalesva" target="_blank" class="book-btn"><i class="fas fa-calendar"></i> Book Discovery Call</a>
  </div>
</header>

<!-- ABOUT -->
<section id="about">
  <img src="gonzales/Gonzales_Michelle.jpg" class="about-img">
  <div class="about-text">
    <h2>Operational Partner</h2>
    <p>I provide administrative and financial documentation support for businesses that need reliable back-office organization. My focus is building structured workflows that keep records organized and easy to manage.</p>
    <p>I am currently expanding my bookkeeping skills and continuing to develop my QuickBooks knowledge while supporting clients with documentation, financial tracking, and administrative coordination.</p>
  </div>
</section>

<!-- PROFESSIONAL ADVANTAGE -->
<section id="value">
  <h2>Professional Advantage</h2>
  <div class="prop-grid">
    <div class="check"><i class="fas fa-check-circle"></i><div><h3>Corporate Discipline</h3><p>Structured documentation and organized records.</p></div></div>
    <div class="check"><i class="fas fa-check-circle"></i><div><h3>Process Organization</h3><p>Reliable workflows for business operations.</p></div></div>
    <div class="check"><i class="fas fa-check-circle"></i><div><h3>Reliable Communication</h3><p>Professional support across teams.</p></div></div>
  </div>
</section>

<!-- CORE EXPERTISE -->
<section id="services">
  <h2>Core Expertise</h2>
  <div class="grid">
    <div class="card"><i class="fas fa-user-tie"></i><h3>Executive Administration</h3><p>Email organization, scheduling, document management.</p></div>
    <div class="card"><i class="fas fa-book"></i><h3>Bookkeeping Support</h3><p>Transaction documentation and financial record organization.</p></div>
    <div class="card"><i class="fas fa-file-invoice-dollar"></i><h3>Accounts Receivable</h3><p>Invoice tracking and payment monitoring.</p></div>
    <div class="card"><i class="fas fa-calculator"></i><h3>Payroll Documentation</h3><p>Organizing payroll records and salary tracking.</p></div>
  </div>
</section>

<!-- WORKFLOW -->
<section id="workflow">
  <h2>Client Onboarding Workflow</h2>
  <div class="flow">
    <div class="flow-card"><div class="step">1</div><h3>Discovery Call</h3><p>Discuss business workflow and needs.</p></div>
    <div class="flow-card"><div class="step">2</div><h3>System Setup</h3><p>Secure access and operational alignment.</p></div>
    <div class="flow-card"><div class="step">3</div><h3>Trial Week</h3><p>1-week paid trial collaboration.</p></div>
    <div class="flow-card"><div class="step">4</div><h3>Full Support</h3><p>Long-term administrative support.</p></div>
  </div>
</section>

<!-- TOOLS -->
<section id="tools">
  <h2>Tech Stack</h2>
  <div class="tools">
    <div class="tool"><img src="logos/Quickbooks.jpg"><p>QuickBooks (Learning)</p></div>
    <div class="tool"><img src="logos/Microsoft_Excel.jpg"><p>Excel</p></div>
    <div class="tool"><img src="logos/Google_Workspace.jpg"><p>Google Workspace</p></div>
    <div class="tool"><img src="logos/ChatGPT.jpg"><p>ChatGPT</p></div>
    <div class="tool"><img src="logos/Canva.jpg"><p>Canva</p></div>
    <div class="tool"><img src="logos/Microsoft_365.jpg"><p>Microsoft 365</p></div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certs">
  <h2>Professional Certifications</h2>
  <div class="certs">
    <div class="cert"><img src="certificates/Canva_Visual_Suite.png"><p>Canva Visual Suite</p></div>
    <div class="cert"><img src="certificates/Introduction_to_Bookkeeping.png"><p>Bookkeeping</p></div>
    <div class="cert"><img src="certificates/Journalizing_Transactions.png"><p>Journalizing</p></div>
    <div class="cert"><img src="certificates/Google_Workspace_Features_and_Applications.png"><p>Google Workspace</p></div>
    <div class="cert"><img src="certificates/Accounts_Receivable_Management.png"><p>AR Management</p></div>
    <div class="cert"><img src="certificates/Accounting_Basics.png"><p>Accounting Basics</p></div>
    <div class="cert"><img src="certificates/Gmail_Calendar_for_Business_Masterclass.png"><p>Executive Admin</p></div>
    <div class="cert"><img src="certificates/Diploma_in_Financial_Accounting.png"><p>Financial Accounting</p></div>
  </div>
</section>

<!-- FAQ -->
<section id="faq">
  <h2>Frequently Asked Questions</h2>
  <div class="faq">
    <div class="faq-item">
      <div class="faq-question"><span>Do you offer trial work?</span><i class="fas fa-chevron-down"></i></div>
      <div class="faq-answer">Yes. I offer a 1-week paid trial to ensure workflow compatibility.</div>
    </div>
    <div class="faq-item">
      <div class="faq-question"><span>Which timezones do you support?</span><i class="fas fa-chevron-down"></i></div>
      <div class="faq-answer">I work with businesses across US, UK, and Australian timezones.</div>
    </div>
    <div class="faq-item">
      <div class="faq-question"><span>How do clients schedule appointments?</span><i class="fas fa-chevron-down"></i></div>
      <div class="faq-answer">Clients can book directly via <a href="https://cal.com/michgonzalesva" target="_blank">Cal.com</a>.</div>
    </div>
    <div class="faq-item">
      <div class="faq-question"><span>What is your payment method?</span><i class="fas fa-chevron-down"></i></div>
      <div class="faq-answer">Payments can be made via bank transfer or PayPal depending on agreement.</div>
    </div>
    <div class="faq-item">
      <div class="faq-question"><span>What software do you use?</span><i class="fas fa-chevron-down"></i></div>
      <div class="faq-answer">I use QuickBooks, Excel, Google Workspace, ChatGPT, Canva, and Microsoft 365.</div>
    </div>
  </div>
</section>

<!-- CTA -->
<section class="cta">
  <h2>Ready to streamline your business operations?</h2>
  <a href="https://cal.com/michgonzalesva" target="_blank" class="btn">Book a Discovery Call</a>
</section>

<!-- FLOATING WHATSAPP -->
<a href="https://wa.me/639654033089" target="_blank" class="whatsapp-float"><i class="fab fa-whatsapp"></i></a>

<script>
// FAQ toggle
document.querySelectorAll(".faq-item").forEach(item=>{
  item.addEventListener("click",()=>{ item.classList.toggle("active"); });
});

// Scroll fade-in effect
const sections = document.querySelectorAll("section");
const observer = new IntersectionObserver(entries=>{
  entries.forEach(entry=>{ if(entry.isIntersecting){ entry.target.classList.add("visible"); } });
}, { threshold: 0.15 });
sections.forEach(section=>observer.observe(section));
</script>

</body>
</html>
