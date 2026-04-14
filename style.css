// Social links (update LinkedIn)
const SOCIAL = {
  linkedin: "https://www.linkedin.com/in/mrrilan/",
  github: "https://github.com/mrmrilan"
};

// Certificates (replace "#" with your real links)
const CERTIFICATES = [
  { 
    title: "Google AI Essentials", 
    meta: "Coursera • Sep 2025", 
    url: "https://www.linkedin.com/posts/mrrilan_google-ai-essentials-activity-7377963441447301120-6Gf3" 
  },
  { 
    title: "Certificate Data Analytics", 
    meta: "NoviTech R&D • May–Jun 2025", 
    url: "https://www.linkedin.com/posts/mrrilan_data-analytics-internship-activity-7405469683027677184-QMIk" 
  },
  { 
    title: "UI/UX Design MasterClass", 
    meta: "NoviTech R&D • Apr–Jun 2025", 
    url: "https://www.linkedin.com/posts/mrrilan_uiux-activity-7344940182531395584-xF5v" 
  },
  { 
    title: "Advanced Excel", 
    meta: "ZIPS Campus • 2024", 
    url: "#" 
  },
  { 
    title: "Web Designing for Beginners", 
    meta: "University of Moratuwa • 2024", 
    url: "https://www.linkedin.com/posts/mrrilan_webdesign-lifelonglearning-universityofmoratuwa-activity-7278390288409051136-mLH2" 
  }
];

// Footer year
document.getElementById("year").textContent = new Date().getFullYear();

// Social buttons
const linkedinLink = document.getElementById("linkedinLink");
const githubLink = document.getElementById("githubLink");
if (linkedinLink) linkedinLink.href = SOCIAL.linkedin;
if (githubLink) githubLink.href = SOCIAL.github;

// Inject progress bar + particles canvas
addProgressBar();
addParticles();

// Mobile nav
const navToggle = document.getElementById("navToggle");
const navMenu = document.getElementById("navMenu");
if (navToggle && navMenu) {
  navToggle.addEventListener("click", () => {
    const isOpen = navMenu.classList.toggle("open");
    navToggle.setAttribute("aria-expanded", String(isOpen));
  });
  navMenu.querySelectorAll("a").forEach(a => {
    a.addEventListener("click", () => {
      navMenu.classList.remove("open");
      navToggle.setAttribute("aria-expanded", "false");
    });
  });
}

// Reveal on scroll
const revealEls = [...document.querySelectorAll(".reveal")];
const io = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.classList.add("is-visible");
      io.unobserve(e.target);
    }
  });
}, { threshold: 0.12 });
revealEls.forEach(el => io.observe(el));

// Real 3D tilt
enable3DTilt();

// Certificates render
renderCertificates();

// Contact form -> mailto
const form = document.getElementById("contactForm");
const formHint = document.getElementById("formHint");
if (form) {
  form.addEventListener("submit", (e) => {
    e.preventDefault();
    const data = new FormData(form);
    const name = String(data.get("name") || "");
    const email = String(data.get("email") || "");
    const message = String(data.get("message") || "");

    const subject = encodeURIComponent(`Portfolio Inquiry from ${name}`);
    const body = encodeURIComponent(`From: ${name} (${email})\n\n${message}`);

    window.location.href = `mailto:rilanmohamed0206@gmail.com?subject=${subject}&body=${body}`;
    if (formHint) formHint.textContent = "Opening your email app…";
  });
}

/* ---------------- helpers ---------------- */

function renderCertificates(){
  const certGrid = document.getElementById("certGrid");
  if (!certGrid) return;

  certGrid.innerHTML = CERTIFICATES.map(c => `
    <div class="certItem">
      <div>
        <div style="font-weight:950">${escapeHtml(c.title)}</div>
        <div style="color:rgba(238,242,255,.72);font-weight:850;font-size:13px">${escapeHtml(c.meta)}</div>
      </div>
      <a class="btn btn--small btn--ghost" target="_blank" rel="noreferrer"
         href="${c.url}">${c.url === "#" ? "Add Link" : "View"}</a>
    </div>
  `).join("");
}

function enable3DTilt(){
  const cards = document.querySelectorAll(".tilt");
  const max = 10; // degrees
  const hasHover = window.matchMedia("(hover:hover)").matches;
  const reduceMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
  if (!hasHover || reduceMotion) return;

  cards.forEach(card => {
    card.addEventListener("mousemove", (e) => {
      const r = card.getBoundingClientRect();
      const px = (e.clientX - r.left) / r.width;
      const py = (e.clientY - r.top) / r.height;

      const rx = (py - 0.5) * -max;
      const ry = (px - 0.5) * max;

      card.style.transform = `perspective(900px) rotateX(${rx}deg) rotateY(${ry}deg) translateY(-2px)`;
    });

    card.addEventListener("mouseleave", () => {
      card.style.transform = "";
    });
  });
}

function addProgressBar(){
  const bar = document.createElement("div");
  bar.className = "progress";
  document.body.appendChild(bar);

  const onScroll = () => {
    const doc = document.documentElement;
    const scrollTop = doc.scrollTop;
    const height = doc.scrollHeight - doc.clientHeight;
    const pct = height > 0 ? (scrollTop / height) * 100 : 0;
    bar.style.width = pct + "%";
  };

  window.addEventListener("scroll", onScroll, { passive: true });
  onScroll();
}

function addParticles(){
  const reduceMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
  if (reduceMotion) return;

  const canvas = document.createElement("canvas");
  canvas.className = "particles";
  document.body.appendChild(canvas);
  const ctx = canvas.getContext("2d");

  const DPR = Math.max(1, Math.min(2, window.devicePixelRatio || 1));
  let w, h;

  const count = 55;
  const dots = Array.from({ length: count }, () => ({
    x: Math.random(),
    y: Math.random(),
    r: 0.6 + Math.random() * 1.6,
    vx: (-0.12 + Math.random() * 0.24),
    vy: (-0.08 + Math.random() * 0.16),
    a: 0.18 + Math.random() * 0.22
  }));

  function resize(){
    w = window.innerWidth; h = window.innerHeight;
    canvas.width = Math.floor(w * DPR);
    canvas.height = Math.floor(h * DPR);
    canvas.style.width = w + "px";
    canvas.style.height = h + "px";
    ctx.setTransform(DPR,0,0,DPR,0,0);
  }
  window.addEventListener("resize", resize);
  resize();

  function step(){
    ctx.clearRect(0,0,w,h);
    for (const d of dots){
      d.x += d.vx / w * 120;
      d.y += d.vy / h * 120;

      if (d.x < -0.1) d.x = 1.1;
      if (d.x > 1.1) d.x = -0.1;
      if (d.y < -0.1) d.y = 1.1;
      if (d.y > 1.1) d.y = -0.1;

      const x = d.x * w;
      const y = d.y * h;

      ctx.beginPath();
      ctx.arc(x, y, d.r, 0, Math.PI * 2);
      ctx.fillStyle = `rgba(238,242,255,${d.a})`;
      ctx.fill();
    }
    requestAnimationFrame(step);
  }
  requestAnimationFrame(step);
}

function escapeHtml(str) {
  return str.replace(/[&<>"']/g, (m) => ({
    "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#039;"
  }[m]));
}
