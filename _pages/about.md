---
permalink: /
title: "Hi, I'm Nazrul 👋"
excerpt: "Software engineer and ML engineer"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a software engineer and ML engineer based in New York City. I build backend systems, ML pipelines, and LLM agents, and I like measuring whether they actually work. I recently finished my MS in Computer Science at Oklahoma State University.

**I am open to Software Engineer, ML Engineer, and AI Engineer roles.**

<div class="stats">
  <div class="stat"><strong>70% → 93%</strong><span>LLM agent task completion</span></div>
  <div class="stat"><strong>45× faster</strong><span>ML document validation</span></div>
  <div class="stat"><strong>80,000+</strong><span>citizens served by APIs I built</span></div>
</div>

<p class="cta">
  <a class="btn btn--info" href="/files/Shanto_Resume.pdf">Download Résumé</a>
  <a class="btn btn--inverse" href="mailto:mshanto@okstate.edu">Email Me</a>
  <a class="btn btn--inverse" href="https://github.com/nazrulhuda">GitHub</a>
  <a class="btn btn--inverse" href="https://www.linkedin.com/in/nazrulhudashanto/">LinkedIn</a>
</p>

# Featured Projects

<div class="card has-media">
  <div>
    <h3>LLM Agent for Zero-Knowledge Proofs</h3>
    <p><b>Problem:</b> LLMs often leave out or invent the exact values that tools need, so an agent can quietly call the wrong backend or act for the wrong user.</p>
    <p><b>What I built:</b> a chat assistant where a LangGraph agent runs a zero-knowledge proof system through 8 custom MCP tools, with 20 server-side checks that complete or override what the model sends.</p>
    <p class="result">Result: task completion rose from 70% to 93%, and all 198 misrouted status checks were removed.</p>
    <div class="tags"><span class="tag">Python</span><span class="tag">LangGraph</span><span class="tag">FastMCP</span><span class="tag">Flask</span><span class="tag">Redis</span><span class="tag">PostgreSQL</span><span class="tag">Docker</span></div>
    <p>
      <a class="btn btn--info btn--small" href="https://github.com/disys-lab/Skeptical-MCP-For-zkSNARKs">Code</a>
      <a class="btn btn--inverse btn--small" href="https://github.com/disys-lab/Skeptical-MCP-For-zkSNARKs/blob/main/manuscript/Natural-Language-ZK-Verification-via-Skeptical-MCP-Tools.pdf">Paper</a>
      <a class="btn btn--inverse btn--small" href="/images/skeptical_architecture.png">Architecture</a>
    </p>
  </div>
  <div class="card-media">
    <a href="/images/skeptical_chat.png"><img src="/images/skeptical_chat.png" alt="The Prover Assistant chat: a user checks whether their data was used, then follows a proof from submission to verification"></a>
  </div>
</div>

<div class="card has-media">
  <div>
    <h3>DDoS Defense for Kubernetes Service Meshes</h3>
    <p><b>Problem:</b> a flood of requests to one microservice can bring a whole app down, and service meshes like Istio only offer fixed rules set by hand.</p>
    <p><b>What I built:</b> a single monitoring pod that reads Envoy telemetry, detects attacks with a separate ML model for each service, and patches Istio routing to move traffic to backup versions, with no changes to application code.</p>
    <p class="result">Result: 94.0–97.8% detection accuracy, and parallel inference made detection 55.9% faster (37.4 ms vs. 84.8 ms).</p>
    <div class="tags"><span class="tag">Python</span><span class="tag">scikit-learn</span><span class="tag">Kubernetes</span><span class="tag">Istio</span><span class="tag">Envoy</span><span class="tag">Prometheus</span></div>
    <p>
      <a class="btn btn--info btn--small" href="https://github.com/nazrulhuda/AI-Driven-Anomaly-Detector-and-mitigation-as-a-service">Prototype code</a>
      <a class="btn btn--inverse btn--small" href="https://drive.google.com/file/d/1KdqIUXU8p5YX9Xib-yazjfmLLQQOJWKe/view?usp=sharing">Paper</a>
    </p>
  </div>
  <div class="card-media">
    <a href="/images/ddos_architecture.jpg"><img src="/images/ddos_architecture.jpg" alt="How the DDoS detection and rerouting framework works"></a>
  </div>
</div>

<div class="card">
  <h3>FwdStar, a Freight Marketplace</h3>
  <p><b>Problem:</b> in Bangladesh, freight is booked offline, through phone calls between shippers, brokers, and carriers.</p>
  <p><b>What I built:</b> as technical lead and sole architect (2026–present, MVP), I turned the client's needs into a technical specification and built the platform in nine phases, from phone-first sign-up to GPS shipment tracking.</p>
  <p class="result">Result: 50+ documented REST endpoints and 20+ PostgreSQL tables, with row locking so a load is never awarded twice.</p>
  <div class="tags"><span class="tag">Next.js</span><span class="tag">TypeScript</span><span class="tag">FastAPI</span><span class="tag">PostgreSQL</span><span class="tag">PostGIS</span><span class="tag">Docker</span></div>
  <p><a class="btn btn--inverse btn--small" href="/projects/">Details</a></p>
</div>

More projects, including a LangChain + MCP chatbot and a license-plate reader, are on the [Projects](/projects/) page.

# Experience

<ul class="timeline">
  <li><b>Graduate Research Assistant</b>, Oklahoma State University<span class="when">Jan 2024 – May 2026</span>Built the LLM agent and the Kubernetes DDoS defense above, and contributed a merged fix to the open-source <a href="https://github.com/disys-lab/cosmetic">CoSMeTIC</a> framework.</li>
  <li><b>AI Instructor</b>, NSF Research Experiences for Teachers, Oklahoma State University<span class="when">May 2025 – Aug 2025</span>Taught Python, machine learning, and Transformers to 10 K–12 teachers.</li>
  <li><b>Junior Software Engineer</b>, Tirzok Private Ltd.<span class="when">Feb 2023 – Dec 2023</span>Led ML document validation for <a href="https://www.cliqloan.com/">CliQloan</a>, 45× faster than manual checks; built APIs for a government portal serving 80,000+ citizens.</li>
  <li><b>Undergraduate Research Assistant</b>, BRAC University<span class="when">Oct 2020 – Jan 2023</span>Built a cloud image retrieval framework that cut user waiting time by up to 54% (IEEE Transactions on Cloud Computing, corresponding author).</li>
</ul>

<p><a class="btn btn--info" href="/files/Shanto_Resume.pdf">Full Résumé</a></p>

# Skills

<div class="skill-group"><b>Languages</b><span class="tag">Python</span><span class="tag">Java</span><span class="tag">TypeScript</span><span class="tag">JavaScript</span><span class="tag">SQL</span><span class="tag">Bash</span></div>
<div class="skill-group"><b>AI & ML</b><span class="tag">LangGraph</span><span class="tag">LangChain</span><span class="tag">MCP</span><span class="tag">PyTorch</span><span class="tag">scikit-learn</span><span class="tag">LIME</span></div>
<div class="skill-group"><b>Backend</b><span class="tag">FastAPI</span><span class="tag">Flask</span><span class="tag">Spring Boot</span><span class="tag">Node.js</span><span class="tag">Next.js</span><span class="tag">REST APIs</span><span class="tag">JWT</span></div>
<div class="skill-group"><b>Cloud & Infrastructure</b><span class="tag">Docker</span><span class="tag">Kubernetes</span><span class="tag">Istio</span><span class="tag">Envoy</span><span class="tag">Prometheus</span><span class="tag">AWS</span></div>
<div class="skill-group"><b>Data</b><span class="tag">PostgreSQL</span><span class="tag">PostGIS</span><span class="tag">Redis</span><span class="tag">MongoDB</span><span class="tag">RabbitMQ</span></div>

# Publications

A first-author paper on the LLM agent above is under review at IEEE BigData 2026, and I am the corresponding author of a paper in *IEEE Transactions on Cloud Computing*. [All publications](/publications/)

# Education

- **M.S. in Computer Science**, Oklahoma State University · 2026 · GPA 3.82/4.0
- **B.S. in Computer Science**, BRAC University · 2022

# Outside Work and Contact

I am the founding captain of **Lagaan**, a cricket team in Stillwater, Oklahoma, which has won two trophies ([Hobbies](/hobbies/)).

<p class="cta">
  <a class="btn btn--info" href="mailto:mshanto@okstate.edu">Email Me</a>
  <a class="btn btn--inverse" href="https://www.linkedin.com/in/nazrulhudashanto/">LinkedIn</a>
</p>
