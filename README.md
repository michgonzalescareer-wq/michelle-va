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

/* --- HERO SECTION (UPDATED) --- */
header { 
    height:70vh; 
    display:flex; 
    flex-direction:column; 
    align-items:center; 
    justify-content:center; 
    text-align:center; 
    /* This matches your file name 'hero_bg' and folder 'hero' */
    /* The gradient creates the dark blue professional overlay */
    background: linear-gradient(rgba(11, 42, 74, 0.88), rgba(11, 42, 74, 0.88)), 
                url("hero/hero_bg.jpg"); 
    background-size:cover; 
    background-position:center; 
}
header h1 { font-size:3.5rem; margin-bottom:10px; }
header p { opacity: 0.9; font-size: 1.1rem; }
.hero-buttons { margin-top:25px; display:flex; gap:15px; flex-wrap:wrap; justify-content:center; }
.hero-buttons a { padding:12px 25px; border-radius:40px; text-decoration:none; color:white; font-weight:600; transition: transform 0.3s; display: flex; align-items: center; gap: 8px; }
.hero-buttons a:hover { transform: scale(1.05); }
.linkedin-btn { background:#0A66C2; }
.whatsapp-btn { background:#25D366; }
.book-btn { background:#1a73e8; }

/* --- ABOUT --- */
#about { background:white; color:#0b2a4a; border-radius:20px; margin-top:-40px; padding:50px; box-shadow:0 10px 30px rgba(0,0,0,.3); display:flex; flex-wrap:wrap; align-items:center; gap:40px; }
.about-img { width:250px; height:250px; object-fit:cover; border-radius:20px; flex-shrink:0; transition: transform 0.3s; }
.about-img:hover { transform: scale(1.05); }
.about-text { flex:1; }
.about-text h2 { color:#0b2a4a; text-align:left; font-size:2rem; margin-bottom:15px; }
.about-text p { margin-top:10px; }

/* --- PROFESSIONAL ADVANTAGE --- */
#value { background:#15417c; border-radius:20px; padding:60px 40px; text-align:center; }
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

/* --- PORTFOLIO / SAMPLE WORKS --- */
.portfolio-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(300px,1fr)); gap:25px; }
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

/* --- FAQ --- */
.faq { max-width:800px; margin:auto; }
.faq-item { background:white; color:#0b2a4a; margin-bottom:15px; border-radius:10px; overflow:hidden; cursor:pointer; }
.faq-question { padding:20px; font-weight:600; display:flex; justify-content:space-between; align-items:center; }
.faq-answer { max-height:0; overflow:hidden; padding:0 20px; transition: max-height 0.3s ease, padding 0.3s ease; }
.faq-item.active .faq-answer { max-height:1000px; padding:20px; }
.faq-question i { transition: transform 0.3s; }
.faq-item.active .faq-question i { transform: rotate(180deg); }

/* --- CTA & CONTACT --- */
.cta { background: linear-gradient(135deg, #1a73e8 0%, #0b2a4a 100%); padding: 100px 40px; border-radius: 30px; text-align: center; margin: 80px 20px; position: relative; overflow: hidden; box-shadow: 0 20px 40px rgba(0,0,0,0.4); }
.cta h2 { color: white; font-size: 2.5rem; margin-bottom: 15px; }
.cta p { font-size: 1.1rem; margin-bottom: 35px; opacity: 0.9; max-width: 600px; margin-left: auto; margin-right: auto; }
.btn-cta { background: #25D366; color: white; padding: 18px 45px; border-radius: 50px; text-decoration: none; font-weight: 700; font-size: 1.2rem; display: inline-flex; align-items: center; gap: 10px; transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275); box-shadow: 0 10px 20px rgba(37, 211, 102, 0.3); }
.btn-cta:hover { transform: scale(1.1) translateY(-3px); background: #20ba5a; }
.cta-contact-grid { display: flex; justify-content: center; gap: 50px; margin-top: 50px; padding-top: 30px; border-top: 1px solid rgba(255, 255, 255, 0.2); flex-wrap: wrap; }
.cta-contact-item { color: white; text-decoration: none; font-size: 1rem; display: flex; align-items: center; gap: 12px; transition: all 0.3s ease; padding: 10px 15px; }
.cta-contact-item:hover { opacity: 0.8; transform: translateY(-2px); }
.cta-contact-item i { color: #7cb9ff; font-size: 1.2rem; }

/* --- FLOATING WHATSAPP --- */
.whatsapp-float { position: fixed; bottom:25px; right:25px; background:#25D366; color:white; font-size:26px; padding:15px 18px; border-radius:50%; box-shadow:0 6px 15px rgba(0,0,0,0.3); z-index:999; display:flex; align-items:center; justify-content:center; text-decoration:none; transition: transform 0.3s; }
.whatsapp-float:hover { transform: scale(1.1); }

@media (max-width: 600px) {
  .cta-contact-grid { flex-direction: column; gap: 20px; }
  header h1 { font-size: 2.2rem; }
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
  <img src="gonzales/Gonzales_Michelle.jpg" class="about-img" alt="Michelle Gonzales">
  <div class="about-text">
    <h2>Operational Partner</h2>
    <p>I specialize in streamlining back-office operations and financial documentation. While I have a strong command of accounting fundamentals, I am currently onboarding QuickBooks into my service suite to provide clients with modern, cloud-based reporting and real-time financial tracking.</p>
    
    
  </div>
</section>

<section id="value">
  <h2>Professional Advantage</h2>
  <div class="prop-grid">
    <div class="check"><i class="fas fa-check-circle"></i><div><h3>Corporate Discipline</h3><p>Structured documentation and organized records.</p></div></div>
    <div class="check"><i class="fas fa-check-circle"></i><div><h3>Process Organization</h3><p>Reliable workflows for business operations.</p></div></div>
    <div class="check"><i class="fas fa-check-circle"></i><div><h3>Reliable Communication</h3><p>Professional support across teams.</p></div></div>
  </div>
</section>

<section id="services">
  <h2>Core Expertise</h2>
  <div class="grid">
    <div class="card"><img src="expertise/admin.jpg" alt="Executive Admin"><h3>Executive Administration</h3><p>Email organization, scheduling, document management.</p></div>
    <div class="card"><img src="expertise/bookkeeping.jpg" alt="Bookkeeping"><h3>Bookkeeping Support</h3><p>Transaction documentation and financial record organization. (Learning QuickBooks)</p></div>
    <div class="card"><img src="expertise/ar.jpg" alt="Accounts Receivable"><h3>Accounts Receivable</h3><p>Invoice tracking and payment monitoring.</p></div>
    <div class="card"><img src="expertise/payroll.jpg" alt="Payroll"><h3>Payroll Documentation</h3><p>Organizing payroll records and salary tracking.</p></div>
  </div>
</section>

<section id="portfolio">
  <h2>Sample Works & Reports</h2>
  <div class="portfolio-grid">
    <div class="portfolio-item">
      <div class="portfolio-img-container"><img src="portfolio/pl_statement.jpg" alt="P&L Statement"></div>
      <div class="portfolio-info">
        <span class="portfolio-tag">QuickBooks Online</span>
        <h3>Profit & Loss Statement</h3>
        <p>Generated monthly financial reports to track net income and operating expenses accurately.</p>
      </div>
    </div>
    <div class="portfolio-item">
      <div class="portfolio-img-container"><img src="portfolio/expenses.jpg" alt="Expense Recording"></div>
      <div class="portfolio-info">
        <span class="portfolio-tag">QuickBooks Online</span>
        <h3>Expense Categorization</h3>
        <p>Organization of daily transactions into proper chart of accounts for tax readiness.</p>
      </div>
    </div>
    <div class="portfolio-item">
      <div class="portfolio-img-container"><img src="portfolio/ar_aging.jpg" alt="A/R Aging"></div>
      <div class="portfolio-info">
        <span class="portfolio-tag">Financial Tracking</span>
        <h3>A/R Aging Reports</h3>
        <p>Monitoring outstanding invoices to ensure healthy cash flow and timely payments.</p>
      </div>
    </div>
  </div>
</section>

<section id="workflow">
  <h2>Client Onboarding Workflow</h2>
  <div class="flow">
    <div class="flow-card"><div class="step">1</div><h3>Discovery Call</h3><p>Discuss business workflow and needs.</p></div>
    <div class="flow-card"><div class="step">2</div><h3>System Setup</h3><p>Secure access and operational alignment.</p></div>
    <div class="flow-card"><div class="step">3</div><h3>Trial Week</h3><p>1-week paid trial collaboration.</p></div>
    <div class="flow-card"><div class="step">4</div><h3>Full Support</h3><p>Long-term administrative support.</p></div>
  </div>
</section>

<section id="tools">
  <h2>Tech Stack</h2>
  <div class="tools">
    <div class="tool"><img src="logos/Quickbooks.jpg" alt="QuickBooks"><p>QuickBooks (Learning)</p></div>
    <div class="tool"><img src="logos/Microsoft_Excel.jpg" alt="Excel"><p>Excel</p></div>
    <div class="tool"><img src="logos/Google_Workspace.jpg" alt="Google Workspace"><p>Google Workspace</p></div>
    <div class="tool"><img src="logos/ChatGPT.jpg" alt="ChatGPT"><p>ChatGPT</p></div>
    <div class="tool"><img src="logos/Canva.jpg" alt="Canva"><p>Canva</p></div>
    <div class="tool"><img src="logos/Microsoft_365.jpg" alt="Microsoft 365"><p>Microsoft 365</p></div>
  </div>
</section>

<section id="faq">
  <h2>Frequently Asked Questions</h2>
  <div class="faq">
    <div class="faq-item"><div class="faq-question"><span>Do you offer trial work?</span><i class="fas fa-chevron-down"></i></div><div class="faq-answer">Yes. I offer a 1-week paid trial to ensure workflow compatibility.</div></div>
    
    <div class="faq-item">
        <div class="faq-question"><span>How do you handle QuickBooks if you are currently learning it?</span><i class="fas fa-chevron-down"></i></div>
        <div class="faq-answer">While I am perfecting the software interface, I have a strong foundation in <strong>Accounting Fundamentals</strong>. I understand debits, credits, and the accounting cycle. The "learning" is simply mastering the QuickBooks system shortcuts—the math and accuracy behind your reports remain my top priority.</div>
    </div>

    <div class="faq-item">
        <div class="faq-question"><span>What is the financial advantage of hiring you now?</span><i class="fas fa-chevron-down"></i></div>
        <div class="faq-answer">Hiring me at this stage allows you to get high-level administrative support at a <strong>growth-friendly rate</strong>. You receive an operational partner who already understands financial logic, saving you the high cost of a senior firm while getting the same level of care.</div>
    </div>

    <div class="faq-item"><div class="faq-question"><span>Which timezones do you support?</span><i class="fas fa-chevron-down"></i></div><div class="faq-answer">I work with businesses across US, UK, and Australian timezones.</div></div>
    <div class="faq-item"><div class="faq-question"><span>Payment methods?</span><i class="fas fa-chevron-down"></i></div><div class="faq-answer">Payments can be made via bank transfer or PayPal depending on agreement.</div></div>
  </div>
</section>

<section class="cta" id="contact">
  <h2>Let's Organize Your Growth</h2>
  <p>Delegate your administrative burden and focus on scaling your business. Ready to see how we can work together?</p>
  
  <a href="https://cal.com/michgonzalesva" target="_blank" class="btn-cta">
    <i class="fas fa-calendar-check"></i> Book Your Discovery Call
  </a>

  <div class="cta-contact-grid">
    <a href="mailto:mitchgonzales.career@gmail.com" class="cta-contact-item">
      <i class="fas fa-envelope"></i> mitchgonzales.career@gmail.com
    </a>
    <a href="https://wa.me/639654033089" target="_blank" class="cta-contact-item">
      <i class="fab fa-whatsapp"></i> +63 965 403 3089
    </a>
    <a href="https://www.linkedin.com/in/michgonzalesva" target="_blank" class="cta-contact-item">
      <i class="fab fa-linkedin"></i> LinkedIn Profile
    </a>
  </div>
</section>

<a href="https://wa.me/639654033089" target="_blank" class="whatsapp-float"><i class="fab fa-whatsapp"></i></a>

<script>
const sections = document.querySelectorAll("section");
const observer = new IntersectionObserver(entries=>{
  entries.forEach(entry=>{ if(entry.isIntersecting){ entry.target.classList.add("visible"); } });
},{ threshold: 0.15 });
sections.forEach(section=>observer.observe(section));

document.querySelectorAll(".faq-item").forEach(item=>{
  item.addEventListener("click", ()=>{ item.classList.toggle("active"); });
});
</script>
</body>
</html>
