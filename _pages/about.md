---
permalink: /
title: "Hi, I'm Nazrul 👋"
excerpt: "Software engineer and ML engineer"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a software engineer and ML engineer in New York City. I like building systems that have to be right: ML pipelines that replace manual checking, backends that thousands of people depend on, and LLM agents that call tools without guessing. I recently finished my MS in Computer Science at Oklahoma State University.

**I am open to Software Engineer, ML Engineer, and AI Engineer roles.**

<div class="stats">
  <div class="stat"><strong>+23 pts</strong><span>LLM agent task completion, 3 model families</span></div>
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
    <p class="meta"><span class="kind kind--research">Research</span> · Oklahoma State University · with Dr. Paritosh Ramanan · 2024–2026</p>
    <h3>An LLM Agent That Calls Tools Without Guessing</h3>
    <p class="hook">LLM agents fail quietly: the model leaves out a parameter or invents one, and the tool still runs, against the wrong backend or for the wrong user.</p>
    <p><b>What I built:</b> a chat assistant where a LangGraph agent operates a zero-knowledge proof system through 8 MCP tools I wrote. I added 20 server-side design decisions that check, fill in or override what the model sends, and tested everything with my own 82-query suite across 3 model families (6,000+ runs).</p>
    <p class="result">Result: task completion rose by about 23 points on each of 3 model families (Qwen 3 32B: 70% → 93%), and the 198 status checks that went to the wrong backend with the fix turned off dropped to 0.</p>
    <div class="tags"><span class="tag">Python</span><span class="tag">LangGraph</span><span class="tag">MCP</span><span class="tag">Flask</span><span class="tag">Redis</span><span class="tag">PostgreSQL</span><span class="tag">Docker</span></div>
    <p>
      <a class="btn btn--info btn--small" href="https://youtu.be/MiPHBLRDVGc">Watch demo (1:55)</a>
      <a class="btn btn--inverse btn--small" href="https://github.com/disys-lab/Skeptical-MCP-For-zkSNARKs">Code</a>
      <a class="btn btn--inverse btn--small" href="https://github.com/disys-lab/Skeptical-MCP-For-zkSNARKs/blob/main/manuscript/Natural-Language-ZK-Verification-via-Skeptical-MCP-Tools.pdf">Paper</a>
      <a class="btn btn--inverse btn--small" href="/images/skeptical_architecture.png">Architecture</a>
    </p>
  </div>
  <div class="card-media">
    <a href="https://youtu.be/MiPHBLRDVGc"><img src="/images/skeptical_demo.gif" alt="Demo: without the fix, the agent says it can't find a proof job that the tracker still shows; with the fix, the same status question returns Status is done. Click to watch the full video."></a>
  </div>
</div>

<div class="card">
  <p class="meta"><span class="kind kind--industry">Industry</span> · Tirzok Private Ltd. · 2023</p>
  <h3>ML Document Validation for a Mortgage Platform</h3>
  <p class="hook">Every mortgage application comes with a stack of borrower documents, and someone had to open and check each one by hand.</p>
  <p><b>What I built:</b> I led an ML pipeline for <a href="https://www.cliqloan.com/">CliQloan</a>, a mortgage loan origination system: classifiers sort each document and trim irrelevant pages, AWS Textract pulls out the key fields, and validation APIs check them automatically.</p>
  <div class="flow"><span>Borrower documents</span><i>→</i><span>Classify type</span><i>→</i><span>Trim pages</span><i>→</i><span>AWS Textract</span><i>→</i><span>Validate fields</span></div>
  <p class="result">Result: 45× faster than manual validation, with lower API costs.</p>
  <div class="tags"><span class="tag">Python</span><span class="tag">scikit-learn</span><span class="tag">AWS Textract</span><span class="tag">Lambda</span><span class="tag">ECR</span><span class="tag">Spring Boot</span><span class="tag">PostgreSQL</span><span class="tag">Amazon MQ</span></div>
  <p><a class="btn btn--inverse btn--small" href="/projects/">Details</a></p>
</div>

<div class="card has-media">
  <div>
    <p class="meta"><span class="kind kind--research">Research</span> · Oklahoma State University · 2024–2026</p>
    <h3>Automatic DDoS Defense for Kubernetes</h3>
    <p class="hook">One flooded microservice can take down a whole app, and a service mesh like Istio only offers fixed rules that someone writes by hand.</p>
    <p><b>What I built:</b> a single monitoring pod that reads each service's traffic from its Envoy sidecar, detects attacks with a separate ML model per service, and patches Istio routing to move traffic to a backup version, then restores it when the attack stops. No application code changes.</p>
    <p class="result">Result: 94.0–97.8% detection accuracy, and parallel inference made each detection cycle 55.9% faster (37.4 ms vs. 84.8 ms).</p>
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
  <p class="meta"><span class="kind kind--industry">Industry</span> · Tirzok Private Ltd. · 2023</p>
  <h3>Backend for a Government–Citizen Portal</h3>
  <p class="hook">A national portal that connects citizens of Bangladesh with government services has to stay fast and give each type of user the right access.</p>
  <p><b>What I built:</b> REST APIs and JWT-based role management for <a href="https://janatarsarkar.gov.bd/">Janatar Sarkar</a>, and I optimized its MongoDB aggregation queries.</p>
  <p class="result">Result: serves 80,000+ citizens, with 40% lower query latency.</p>
  <div class="tags"><span class="tag">Node.js</span><span class="tag">MongoDB</span><span class="tag">JWT</span><span class="tag">REST APIs</span></div>
</div>

<div class="card">
  <p class="meta"><span class="kind kind--project">Project</span> · Technical lead and sole architect · 2026–present · MVP</p>
  <h3>FwdStar: A Freight Marketplace, from Spec to MVP</h3>
  <p class="hook">In Bangladesh, freight is still booked offline between shippers, brokers, and carriers.</p>
  <p><b>What I built:</b> I turned the client's verbal needs into a technical specification and built the platform in nine phases: phone-first sign-up, fleet management, a load board, awards, GPS shipment tracking, and SMS alerts, with an English and Bengali frontend.</p>
  <p class="result">Result: 50+ documented REST endpoints and 20+ PostgreSQL tables, with row-level locking so a load is never awarded twice.</p>
  <div class="tags"><span class="tag">Next.js</span><span class="tag">TypeScript</span><span class="tag">FastAPI</span><span class="tag">PostgreSQL</span><span class="tag">PostGIS</span><span class="tag">Docker</span></div>
  <p><a class="btn btn--inverse btn--small" href="/projects/">Details</a></p>
</div>

Smaller builds, including a LangChain + MCP chatbot and a license-plate reader, are on the [Projects](/projects/) page.

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
