<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ReceptAI — AI Receptionist + WhatsApp CRM for Indian SMEs</title>
<meta name="description" content="Never miss a customer call again. AI Receptionist answers in English, books appointments, sends WhatsApp confirmations — 24/7. For clinics, salons, coaching, real estate, auto service & more. Starting at ₹1,499/mo.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --primary:#5b4cf2;
  --primary-dark:#4338ca;
  --green:#16a34a;
  --bg:#f8f9fe;
  --text:#111827;
  --muted:#64748b;
  --card:#ffffff;
  --border:#e5e7eb;
  --amber:#fef3c7;
}
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Inter',system-ui,-apple-system,Segoe UI,Arial,sans-serif;color:var(--text);background:#fff;line-height:1.65;-webkit-font-smoothing:antialiased}
a{color:inherit;text-decoration:none}
.container{max-width:1040px;margin:0 auto;padding:0 24px}

/* NAV */
.nav{position:sticky;top:0;z-index:50;background:rgba(255,255,255,.92);backdrop-filter:blur(10px);border-bottom:1px solid var(--border)}
.nav-inner{display:flex;align-items:center;justify-content:space-between;padding:14px 24px;max-width:1040px;margin:0 auto}
.logo{font-weight:800;font-size:1.15rem;letter-spacing:-.02em}
.logo span{color:var(--primary)}
.nav-links{display:flex;gap:24px;font-size:.92rem;color:#374151}
.nav-links a{text-decoration:none}
.nav-links a:hover{color:var(--primary)}
.nav-cta{color:#374151 !important;font-weight:600;font-size:.88rem}

/* HERO */
.hero{background:linear-gradient(180deg,#f5f3ff 0%, #ffffff 100%);padding:88px 0 64px;text-align:center}
.hero h1{font-size:3rem;line-height:1.12;letter-spacing:-.03em;font-weight:800;max-width:760px;margin:0 auto}
.hero h1 em{color:var(--primary);font-style:normal}
.hero .sub{font-size:1.18rem;color:#475569;max-width:640px;margin:18px auto 30px}
.trust{margin-top:18px;color:var(--muted);font-size:.88rem}
.pill-row{margin-top:22px;display:flex;flex-wrap:wrap;gap:8px;justify-content:center}
.pill{background:#eef2ff;color:#3730a3;padding:6px 13px;border-radius:999px;font-size:.8rem;font-weight:600}

/* contact box */
.contact-box{display:inline-block;background:#fff;border:1.5px solid var(--border);border-radius:16px;padding:18px 26px;box-shadow:0 6px 24px rgba(0,0,0,.06);text-align:left;max-width:520px}
.contact-box strong{display:block;font-size:.8rem;text-transform:uppercase;letter-spacing:.05em;color:var(--muted);margin-bottom:6px}
.contact-box .contact-line{font-weight:600;font-size:1.02rem;color:#1f2937}
.contact-box .contact-line span{color:var(--muted);font-weight:500}

/* SECTIONS */
section{padding:72px 0}
.section-muted{background:var(--bg)}
h2{font-size:2rem;letter-spacing:-.02em;text-align:center;margin-bottom:10px}
.section-lead{text-align:center;color:var(--muted);max-width:620px;margin:0 auto 36px}

/* Industries */
.industries{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:14px}
.industry{background:var(--card);border:1px solid var(--border);border-radius:14px;padding:18px 16px;text-align:center;font-weight:600}
.industry small{display:block;font-weight:500;color:var(--muted);margin-top:4px;font-size:.82rem}

/* 2 col problem/solution */
.split{display:grid;grid-template-columns:1fr 1fr;gap:22px}
.split-card{background:#fff;border-radius:16px;padding:26px;border:1px solid var(--border)}
.split-card.bad{border-left:4px solid #ef4444}
.split-card.good{border-left:4px solid #16a34a}
.split-card h3{margin-bottom:10px;font-size:1.15rem}
.split-card ul{list-style:none;color:#374151}
.split-card ul li{padding:7px 0;padding-left:22px;position:relative}
.split-card ul li::before{content:"—";position:absolute;left:0;color:#9ca3af}

/* Features grid */
.features{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
.feature{background:#fff;border:1px solid var(--border);border-radius:14px;padding:22px}
.feature b{display:block;margin-bottom:6px}
.feature p{color:#4b5563;font-size:.93rem}

/* How it works */
.steps{max-width:720px;margin:0 auto;display:flex;flex-direction:column;gap:14px}
.step{display:flex;gap:16px;background:#fff;border:1px solid var(--border);border-radius:14px;padding:18px 20px;align-items:flex-start}
.step-num{background:#ede9fe;color:#5b21b6;min-width:38px;height:38px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:.92rem}
.step h4{font-size:1rem;margin-bottom:2px}
.step p{color:#4b5563;font-size:.93rem;margin:0}

/* ROI */
.roi-box{max-width:720px;margin:0 auto;background:linear-gradient(135deg,#fff7d6,#ffe68a);border-radius:18px;padding:32px;text-align:center;border:1px solid #fcd34d}
.roi-box .big{font-size:2.3rem;font-weight:800;color:#92400e}
.roi-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px;max-width:680px;margin:22px auto 0;text-align:left;font-size:.93rem;color:#44403c}

/* Pricing */
.pricing-wrap{display:grid;grid-template-columns:1fr 1fr;gap:22px;max-width:820px;margin:0 auto}
.price-card{background:#fff;border:1.5px solid var(--border);border-radius:18px;padding:32px}
.price-card.featured{border:2.5px solid var(--primary);box-shadow:0 12px 40px rgba(91,76,242,.12);position:relative}
.featured-badge{position:absolute;top:-12px;right:20px;background:var(--primary);color:#fff;font-size:.72rem;font-weight:700;padding:4px 12px;border-radius:999px;text-transform:uppercase;letter-spacing:.04em}
.price-card h3{font-size:1.15rem;margin-bottom:4px}
.price-amt{font-size:2.4rem;font-weight:800;margin:8px 0}
.price-amt span{font-size:.95rem;color:var(--muted);font-weight:500}
.price-features{list-style:none;margin:18px 0;color:#374151;font-size:.93rem}
.price-features li{padding:6px 0}
.price-features li::before{content:"✓ ";color:#16a34a;font-weight:700}
.price-cta-box{background:#f8f9fe;border:1px dashed #c7c9d6;border-radius:12px;padding:16px;text-align:center;font-size:.92rem;color:#374151}

/* Comparison */
table.compare{width:100%;border-collapse:collapse;background:#fff;border-radius:14px;overflow:hidden;box-shadow:0 2px 16px rgba(0,0,0,.05)}
.compare th,.compare td{padding:13px 16px;border-bottom:1px solid var(--border);text-align:left;font-size:.93rem}
.compare th{background:#fafafa;color:#374151;font-weight:650}
.compare td strong{color:#16a34a}

/* FAQ */
.faq{max-width:740px;margin:0 auto}
.faq-item{border-bottom:1px solid var(--border);padding:16px 0}
.faq-q{font-weight:600}
.faq-a{color:#4b5563;font-size:.93rem;margin-top:6px}

/* CTA band */
.cta-band{background:linear-gradient(135deg,#5b4cf2,#7c3aed);color:#fff;text-align:center;padding:64px 24px}
.cta-band h2{color:#fff}
.cta-band p{opacity:.92;max-width:560px;margin:8px auto 22px}
.cta-contact{display:inline-block;background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.28);border-radius:14px;padding:16px 24px;font-weight:500}

/* Footer */
footer{background:#0f172a;color:#cbd5e1;padding:48px 0 32px;font-size:.9rem}
footer a{color:#93c5fd;text-decoration:none}
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:24px;max-width:1040px;margin:0 auto;padding:0 24px}
.footer-grid h4{color:#fff;font-size:.92rem;margin-bottom:10px}
.footer-grid ul{list-style:none;color:#94a3b8}
.footer-grid ul li{padding:4px 0}
.copy{border-top:1px solid #1f2937;margin-top:28px;padding-top:18px;text-align:center;color:#64748b;font-size:.82rem}

/* responsive */
@media(max-width:860px){
  .features{grid-template-columns:1fr 1fr}
  .split{grid-template-columns:1fr}
  .pricing-wrap{grid-template-columns:1fr}
  .footer-grid{grid-template-columns:1fr 1fr}
  .hero h1{font-size:2.2rem}
  .nav-links{display:none}
}
@media(max-width:560px){
  .features{grid-template-columns:1fr}
  .footer-grid{grid-template-columns:1fr}
  .hero{padding:64px 0 48px}
  .hero h1{font-size:1.85rem}
}
</style>
</head>
<body>

<!-- NAV -->
<nav class="nav">
  <div class="nav-inner">
    <div class="logo">Recept<span>AI</span></div>
    <div class="nav-links">
      <a href="#industries">Industries</a>
      <a href="#how">How it works</a>
      <a href="#pricing">Pricing</a>
      <a href="#faq">FAQ</a>
    </div>
    <div class="nav-cta">₹1,499/mo</div>
  </div>
</nav>

<!-- HERO -->
<header class="hero">
  <div class="container">
    <h1>Your AI Receptionist for <em>every customer call</em></h1>
    <p class="sub">AI Voice + WhatsApp CRM built for Indian SMEs. Answers in English, books appointments, sends confirmations — 24/7. No missed calls. No missed revenue.</p>
    
    <div class="contact-box">
      <strong>Start your 14-day free trial</strong>
      <div class="contact-line">📞 Call: +91 72081 41283</div>
      <div class="contact-line">💬 WhatsApp: +91 72081 41283</div>
      <div class="contact-line">✉️ Email: sujaljain299@gmail.com</div>
    </div>

    <div class="trust">14-day free trial • Setup in 30 minutes • Cancel anytime • No credit card</div>
    <div class="pill-row">
      <span class="pill">English-first AI</span>
      <span class="pill">WhatsApp CRM</span>
      <span class="pill">Appointment booking</span>
      <span class="pill">Owner dashboard</span>
      <span class="pill">Made in India</span>
    </div>
  </div>
</header>

<!-- INDUSTRIES -->
<section id="industries">
  <div class="container">
    <h2>Built for every local business in India</h2>
    <p class="section-lead">If customers call you to book — ReceptAI works for you. Pre-trained for your industry on day one.</p>
    <div class="industries">
      <div class="industry">🦷 Dental Clinics<small>Checkups, RCT, braces</small></div>
      <div class="industry">💇 Beauty Salons<small>Hair, facial, bridal</small></div>
      <div class="industry">📚 Coaching Institutes<small>Admissions, batches, fees</small></div>
      <div class="industry">🏠 Real Estate Agents<small>Site visits, listings</small></div>
      <div class="industry">🔧 Auto Service Centers<small>Service bookings</small></div>
      <div class="industry">⚖️ Lawyers / CAs<small>Consultation slots</small></div>
      <div class="industry">🏥 Skin / Eye Clinics<small>Consultations</small></div>
      <div class="industry">🍽️ Restaurants<small>Table reservations</small></div>
    </div>
  </div>
</section>

<!-- PROBLEM / SOLUTION -->
<section class="section-muted">
  <div class="container">
    <h2>Stop losing customers to missed calls</h2>
    <p class="section-lead">Indian SMEs lose 30–60% of inbound calls. That’s direct revenue walking to competitors.</p>
    <div class="split">
      <div class="split-card bad">
        <h3>Without ReceptAI</h3>
        <ul>
          <li>Missed calls during busy hours / lunch / after-close</li>
          <li>Customers get frustrated, book with competitors</li>
          <li>Receptionist costs ₹15,000+/mo, works 8 hours</li>
          <li>No lead tracking, no follow-ups</li>
          <li>No-shows because customers forget</li>
        </ul>
      </div>
      <div class="split-card good">
        <h3>With ReceptAI</h3>
        <ul>
          <li>AI answers every message & call, 24/7</li>
          <li>Professional English conversation</li>
          <li>Books appointments automatically</li>
          <li>WhatsApp confirmation + reminders</li>
          <li>Daily lead dashboard for the owner</li>
          <li>Google review collection built-in</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- FEATURES -->
<section id="features">
  <div class="container">
    <h2>Everything you need, nothing you don’t</h2>
    <p class="section-lead">A complete AI receptionist stack, purpose-built for Indian SMEs.</p>
    <div class="features">
      <div class="feature"><b>🤖 AI WhatsApp Agent</b><p>Answers FAQs, pricing, timings, and availability in clear English. Sounds human, never rude.</p></div>
      <div class="feature"><b>📅 Smart Booking</b><p>Captures name, phone, service, and preferred time. Confirms instantly. Cancels/reschedules on command.</p></div>
      <div class="feature"><b>📱 WhatsApp CRM</b><p>Auto-confirmations, 24h reminders, post-visit follow-ups, and review requests — all on WhatsApp.</p></div>
      <div class="feature"><b>📊 Owner Dashboard</b><p>See today’s appointments, new leads, and conversion rate. Mobile-friendly. Shareable with your team.</p></div>
      <div class="feature"><b>🔔 Instant Alerts</b><p>New booking? You get a WhatsApp summary immediately with full customer details.</p></div>
      <div class="feature"><b>🌐 Multi-industry ready</b><p>Clinics, salons, coaching, real estate, auto, legal — pre-configured templates. Add your business in 5 minutes.</p></div>
    </div>
  </div>
</section>

<!-- HOW IT WORKS -->
<section id="how" class="section-muted">
  <div class="container">
    <h2>How it works</h2>
    <p class="section-lead">Live in 30 minutes. No app install for customers. Uses your existing WhatsApp number.</p>
    <div class="steps">
      <div class="step"><div class="step-num">1</div><div><h4>Customer messages your business WhatsApp</h4><p>Your existing number. No change in how customers reach you.</p></div></div>
      <div class="step"><div class="step-num">2</div><div><h4>AI replies instantly</h4><p>Answers services, pricing, and slots — trained on your business info.</p></div></div>
      <div class="step"><div class="step-num">3</div><div><h4>Appointment is booked</h4><p>Name, service, time — all captured and stored automatically.</p></div></div>
      <div class="step"><div class="step-num">4</div><div><h4>Both sides get WhatsApp confirmation</h4><p>Customer gets booking details. You get a lead alert with full context.</p></div></div>
      <div class="step"><div class="step-num">5</div><div><h4>Automatic reminders & follow-up</h4><p>Reduces no-shows. Collects feedback and Google reviews post-visit.</p></div></div>
    </div>
  </div>
</section>

<!-- ROI -->
<section>
  <div class="container">
    <h2>ROI that pays for itself on Day 1</h2>
    <div class="roi-box">
      <div class="big">₹1,499 / month</div>
      <p style="margin-top:8px;color:#44403c">That’s ₹50/day.</p>
      <div class="roi-grid">
        <div><b>Typical SME without AI:</b><br>5 missed calls/day × ₹1,500 avg = ₹7,500/day lost<br>≈ ₹2.25 Lakh/month leaking</div>
        <div><b>With ReceptAI:</b><br>0 missed calls<br>More bookings, fewer no-shows<br>Recovered revenue: ₹50k–₹3L+/mo</div>
      </div>
    </div>
  </div>
</section>

<!-- COMPARISON -->
<section class="section-muted">
  <div class="container" style="max-width:860px">
    <h2>Human receptionist vs ReceptAI</h2>
    <table class="compare" style="margin-top:24px">
      <tr><th>Feature</th><th>Human Receptionist</th><th>ReceptAI</th></tr>
      <tr><td>Monthly cost</td><td>₹15,000+</td><td><strong>₹1,499</strong></td></tr>
      <tr><td>Working hours</td><td>8 hrs</td><td><strong>24/7</strong></td></tr>
      <tr><td>Sick leave / attrition</td><td>Yes</td><td><strong>Never</strong></td></tr>
      <tr><td>Concurrent calls</td><td>1 at a time</td><td><strong>Unlimited</strong></td></tr>
      <tr><td>Languages</td><td>Usually 1</td><td><strong>English</strong></td></tr>
      <tr><td>WhatsApp follow-ups</td><td>Manual</td><td><strong>Automatic</strong></td></tr>
      <tr><td>Daily lead reports</td><td>No</td><td><strong>Auto</strong></td></tr>
    </table>
  </div>
</section>

<!-- PRICING -->
<section id="pricing">
  <div class="container">
    <h2>Simple, transparent pricing</h2>
    <p class="section-lead">Start free. Upgrade when you see the results. Cancel anytime.</p>
    <div class="pricing-wrap">
      <div class="price-card featured">
        <div class="featured-badge">Most Popular</div>
        <h3>Starter</h3>
        <p style="color:var(--muted);font-size:.9rem">Perfect for single-location SMEs</p>
        <div class="price-amt">₹1,499 <span>/ month</span></div>
        <ul class="price-features">
          <li>24/7 AI WhatsApp receptionist</li>
          <li>English conversation</li>
          <li>Unlimited conversations</li>
          <li>Appointment booking & reminders</li>
          <li>Owner dashboard & lead export</li>
          <li>WhatsApp alerts for new bookings</li>
          <li>14-day free trial</li>
        </ul>
        <div class="price-cta-box">
          <strong>Start your free trial</strong><br>
          📞 +91 72081 41283<br>
          💬 WhatsApp: +91 72081 41283<br>
          ✉️ Email: Sujaljain299@gmail.com<br>
        </div>
      </div>
      <div class="price-card">
        <h3>Growth</h3>
        <p style="color:var(--muted);font-size:.9rem">For multi-location / high volume</p>
        <div class="price-amt">₹3,999 <span>/ month</span></div>
        <ul class="price-features">
          <li>Everything in Starter, plus:</li>
          <li>Multi-location / multi-staff routing</li>
          <li>Custom AI training on your FAQs</li>
          <li>Voice calling agent (Phase 2)</li>
          <li>API access & CRM integrations</li>
          <li>Priority support</li>
          <li>Dedicated onboarding</li>
        </ul>
        <div class="price-cta-box">
          <strong>Book a demo call</strong><br>
          📞 +91 72081 41283<br>
          💬 WhatsApp: +91 72081 41283<br>
          ✉️ Email : Sujaljain299@gmail.com<br>
        </div>
      </div>
    </div>
    <p style="text-align:center;margin-top:16px;color:var(--muted);font-size:.88rem">All prices ex-GST. Annual plan: 2 months free.</p>
  </div>
</section>

<!-- FAQ -->
<section id="faq" class="section-muted">
  <div class="container">
    <h2>Frequently asked questions</h2>
    <div class="faq">
      <div class="faq-item"><div class="faq-q">Is this only for clinics / doctors?</div><div class="faq-a">No. ReceptAI works for any local SME where customers call or message to book: salons, coaching institutes, real estate agents, auto service centers, lawyers/CAs, restaurants, and more. We pre-configure it for your industry.</div></div>
      <div class="faq-item"><div class="faq-q">What languages does the AI support?</div><div class="faq-a">The AI is optimized for English. Hindi support is available on request for Growth plan customers.</div></div>
      <div class="faq-item"><div class="faq-q">Do I need to change my phone number?</div><div class="faq-a">No. We connect to your existing WhatsApp Business number via the official WhatsApp API. Customers keep messaging the same number.</div></div>
      <div class="faq-item"><div class="faq-q">What about voice calling?</div><div class="faq-a">The WhatsApp AI agent is live today. AI voice calling is coming in Phase 2 for Growth plan customers.</div></div>
      <div class="faq-item"><div class="faq-q">How fast is setup?</div><div class="faq-a">About 30 minutes. Send us your services, pricing, timings, and address — we configure your AI agent the same day.</div></div>
      <div class="faq-item"><div class="faq-q">Is there a free trial?</div><div class="faq-a">Yes — 14 days, full features, no credit card required. Contact us to start.</div></div>
    </div>
  </div>
</section>

<!-- CTA BAND -->
<section class="cta-band">
  <div class="container">
  <h2>Ready to never miss a customer again?</h2>
  <p>Join fast-growing Indian SMEs using ReceptAI to capture every lead, 24/7. Setup in 30 minutes. 14-day free trial.</p>
  <div class="cta-contact">
    📞 Call: +91 72081 41283 &nbsp;•&nbsp; 💬 WhatsApp: +91 72081 41283 &nbsp;•&nbsp; ✉️ Email: Sujaljain299@gmail.com &nbsp;•&nbsp; 
  </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div>
      <div style="font-weight:800;font-size:1.1rem;margin-bottom:8px">ReceptAI</div>
      <p style="color:#94a3b8;max-width:280px">AI Voice Receptionist + WhatsApp CRM for Indian SMEs. Never miss a customer call again.</p>
      <p style="margin-top:12px;color:#cbd5e1">
        📞 +91 72081 41283<br>
        💬 WhatsApp: +91 72081 41283<br>
        ✉️ Email: Sujaljain299@gmail.com<br>
      </p>
    </div>
    <div>
      <h4>Product</h4>
      <ul><li>Features</li><li>Pricing</li><li>How it works</li><li>FAQ</li></ul>
    </div>
    <div>
      <h4>Industries</h4>
      <ul><li>Clinics & Hospitals</li><li>Beauty Salons</li><li>Coaching Institutes</li><li>Real Estate</li><li>Auto Service</li><li>Lawyers / CAs</li></ul>
    </div>
    <div>
      <h4>Contact</h4>
      <ul style="color:#cbd5e1">
        <li>+91 72081 41283</li>
        <li> Sujaljain299@gmail.com</li>
        <li style="margin-top:8px;color:#94a3b8">14-day free trial<br>No credit card</li>
      </ul>
    </div>
  </div>
  <div class="copy">© 2025 ReceptAI — Made in India • All prices in INR, ex-GST</div>
</footer>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script></body>
</html>

