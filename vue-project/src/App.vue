<script setup lang="ts">
import BackgroundMesh from './components/BackgroundMesh.vue'
import GlassCard from './components/GlassCard.vue'
import ScrollReveal from './components/ScrollReveal.vue'
</script>

<template>
  <BackgroundMesh />
  
  <main class="resume-container">
    <header class="header animate-fade-in">
      <h1 class="name">JOY IDIKA</h1>
      <p class="title">Business Sales Analyst | Business Administration | Business Strategy</p>
      
      <div class="contact-info">
        <span class="contact-link">+44 7423 177098</span>
        <span class="separator">|</span>
        <a href="mailto:Joyidika1990@gmail.com" class="contact-link">Joyidika1990@gmail.com</a>
        <span class="separator">|</span>
        <a href="https://linkedin.com/in/idikajoynkwachinkwachi" target="_blank" class="contact-link">LinkedIn</a>
      </div>
    </header>

    <div class="content-grid">
      <ScrollReveal class="full-width">
        <GlassCard>
          <h2 class="section-title">Professional Profile</h2>
          <p class="section-content">
            Analytical and commercially driven Business Sales Analyst with strong foundations in Business administration, strategic problem-solving, customer insight and operational optimisation across banking and insurance sectors. Two-time Gold Award recipient at AXA for outstanding performance. Proven ability to apply quantitative reasoning and sound judgement to identify opportunities, reduce risk and improve business performance. A confident communicator who thrives in collaborative teams and is highly motivated to build a long-term career.
          </p>
        </GlassCard>
      </ScrollReveal>

      <ScrollReveal class="full-width">
        <GlassCard>
          <h2 class="section-title">Professional Experience</h2>
          
          <div class="experience-item">
            <h3 class="job-title">Business Administration (APPS/Operations) Contract</h3>
            <p class="company">HMCTS – Ministry of Justice, UK | Jun 2025 – Present</p>
            <ul class="bullet-list">
              <li>Supported senior stakeholders through coordination of workflows, documentations and reporting</li>
              <li>Maintained and improved administrative processes to enhance operational efficiency by using case Man, PowerApps, finance portal, for case progression and records management</li>
            </ul>
          </div>

          <div class="experience-item">
            <h3 class="job-title">Business Support Analyst</h3>
            <p class="company">Ruthad Limited, UK | Feb 2023 – Jun 2025</p>
            <ul class="bullet-list">
              <li>Used data and process analysis to redesign CRM workflows, reducing customer response times from 16 days to 5 days</li>
              <li>Conducted problem analysis, option evaluation and benefits assessment to support leadership decisions</li>
              <li>Prioritised backlogs, success measures and delivery roadmaps to track performance improvements</li>
            </ul>
          </div>

          <div class="experience-item">
            <h3 class="job-title">Business Sales Analyst</h3>
            <p class="company">AXA Mansard Insurance | Oct 2020 – Feb 2023</p>
            <ul class="bullet-list">
              <li>Analysed sales performance and market trends</li>
              <li>Supported digital and product strategy initiatives that contributed to a 70% increase in policy sales</li>
              <li>Produced insight reports to support senior management decision-making</li>
              <li>Recognised with two AXA Gold Awards for outstanding performance and analytical contribution</li>
            </ul>
          </div>

          <div class="experience-item">
            <h3 class="job-title">Business Sales Analyst</h3>
            <p class="company">Sterling Bank | Jan 2019 – Aug 2020</p>
            <ul class="bullet-list">
              <li>Analysed lending portfolio data to support risk management and credit optimisation initiatives</li>
              <li>Contributed to improved operational controls resulting in a 60% reduction in non-performing loans</li>
              <li>Worked cross-functionally with IT and compliance teams to enhance digital systems and process efficiency</li>
            </ul>
          </div>
        </GlassCard>
      </ScrollReveal>

      <ScrollReveal>
        <GlassCard>
          <h2 class="section-title">Core Skills</h2>
          <ul class="skills-list">
            <li>Data-driven decision making</li>
            <li>Business case development</li>
            <li>Performance analysis and insight generation</li>
            <li>Opportunity identification</li>
            <li>Risk and impact assessment</li>
            <li>Advanced Excel for analysis, dashboards and reporting</li>
            <li>Data interpretation and trend analysis</li>
            <li>CRM analytics</li>
            <li>Process performance measurement</li>
            <li>Customer behaviour analysis</li>
            <li>Growth strategy support</li>
            <li>Service optimisation and benefits realisation</li>
            <li>Agile delivery</li>
            <li>Stakeholder engagement</li>
            <li>Cross-functional collaboration</li>
            <li>Workshop facilitation</li>
            <li>Professional communication</li>
          </ul>
        </GlassCard>
      </ScrollReveal>

      <ScrollReveal>
        <GlassCard>
          <h2 class="section-title">Education & Certifications</h2>
          
          <div class="education-item">
            <h3 class="degree">MBA</h3>
            <p class="institution">University of Northampton</p>
          </div>

          <h3 class="cert-title">Professional Certifications</h3>
          <ul class="cert-list">
            <li>CMI Level 7 Diploma – Strategic Management & Leadership Practice</li>
            <li>Business Analysis Foundation</li>
            <li>Strategic Business Analysis Essentials</li>
            <li>Business Process Improvement</li>
          </ul>
        </GlassCard>
      </ScrollReveal>

    </div>
  </main>
</template>

<style>
.resume-container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 3rem 2rem;
  position: relative;
  z-index: 1;
}

.header {
  text-align: center;
  margin-bottom: 3rem;
}

.name {
  font-size: 3rem;
  font-weight: 700;
  color: #ffffff;
  letter-spacing: 0.1em;
  margin-bottom: 0.5rem;
  background: linear-gradient(135deg, #06b6d4, #3b82f6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.title {
  font-size: 1.2rem;
  color: #94a3b8;
  margin-bottom: 1.5rem;
}

.contact-info {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 0.5rem;
  font-size: 0.95rem;
}

.contact-link {
  color: #06b6d4;
  text-decoration: none;
  transition: color 0.3s ease;
}

.contact-link:hover {
  color: #22d3ee;
}

.separator {
  color: #475569;
}

.content-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
}

.full-width {
  grid-column: 1 / -1;
}

.section-title {
  font-size: 1.4rem;
  font-weight: 600;
  color: #06b6d4;
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid rgba(6, 182, 212, 0.3);
}

.section-content {
  color: #e2e8f0;
  line-height: 1.7;
  font-size: 0.95rem;
}

.experience-item {
  margin-bottom: 1.5rem;
}

.experience-item:last-child {
  margin-bottom: 0;
}

.job-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #f1f5f9;
  margin-bottom: 0.25rem;
}

.company {
  color: #94a3b8;
  font-size: 0.9rem;
  margin-bottom: 0.75rem;
}

.bullet-list {
  list-style-type: disc;
  padding-left: 1.5rem;
  color: #cbd5e1;
}

.bullet-list li {
  margin-bottom: 0.5rem;
  line-height: 1.5;
  font-size: 0.9rem;
}

.skills-list {
  list-style-type: none;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.skills-list li {
  background: rgba(6, 182, 212, 0.15);
  border: 1px solid rgba(6, 182, 212, 0.3);
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  color: #e2e8f0;
}

.education-item {
  margin-bottom: 1.5rem;
}

.degree {
  font-size: 1.1rem;
  font-weight: 600;
  color: #f1f5f9;
  margin-bottom: 0.25rem;
}

.institution {
  color: #94a3b8;
  font-size: 0.9rem;
}

.cert-title {
  font-size: 1rem;
  font-weight: 600;
  color: #f1f5f9;
  margin-bottom: 0.75rem;
}

.cert-list {
  list-style-type: disc;
  padding-left: 1.5rem;
  color: #cbd5e1;
}

.cert-list li {
  margin-bottom: 0.5rem;
  line-height: 1.5;
  font-size: 0.9rem;
}

.animate-fade-in {
  animation: fadeIn 0.4s ease-out forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .content-grid {
    grid-template-columns: 1fr;
  }
  
  .name {
    font-size: 2rem;
  }
  
  .contact-info {
    flex-direction: column;
    align-items: center;
  }
  
  .separator {
    display: none;
  }
}
</style>
