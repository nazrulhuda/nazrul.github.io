---
permalink: /
title: "Hi, I'm Nazrul 👋"
excerpt: "Software engineer and ML engineer"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a software engineer and ML engineer based in New York City. I build backend systems, ML pipelines, and LLM agents. At Tirzok, I led an ML document-validation system for a mortgage loan origination system that ran **45× faster** than checking documents by hand, and I built the backend of a government portal that serves **80,000+ citizens**. During my MS in Computer Science at Oklahoma State University, I built an LLM agent that runs zero-knowledge proof systems through custom MCP tools, and an ML system that detects DDoS attacks on Kubernetes and reroutes traffic automatically.

**I am open to Software Engineer, ML Engineer, and AI Engineer roles.**  
[Projects](/projects/) · [GitHub](https://github.com/nazrulhuda) · [LinkedIn](https://www.linkedin.com/in/nazrulhudashanto/) · [Email](mailto:mshanto@okstate.edu)

## Skills

- **Languages:** Python, Java, TypeScript/JavaScript, SQL, Bash
- **Backend & APIs:** FastAPI, Flask, Spring Boot, Node.js, Next.js, REST APIs, JWT-based access control
- **AI & ML:** LangGraph, LangChain, Model Context Protocol (FastMCP), ReAct agents, scikit-learn, PyTorch, LIME
- **Cloud & Infrastructure:** Docker, Kubernetes, Istio/Envoy, Prometheus, AWS (Lambda, ECR, Textract, Amazon MQ)
- **Data:** PostgreSQL and PostGIS, Redis, MongoDB, RabbitMQ

# Experience

## Junior Software Engineer · Tirzok Private Ltd.

*Dhaka, Bangladesh · Feb 2023 – Dec 2023*

- **ML document validation for [CliQloan](https://www.cliqloan.com/)**, AmitaSoft's mortgage loan origination system. I led a system where ML classifiers identify each document's type, a page-trimming model removes irrelevant pages, AWS Textract extracts the key fields, and a validation service checks them. It runs **45× faster than manual validation** and lowers API costs. *(scikit-learn, AWS Textract, Lambda, ECR, Amazon MQ, Spring Boot, PostgreSQL)*
- **Backend of [Janatar Sarkar](https://janatarsarkar.gov.bd/)**, a government–citizen portal serving **80,000+ citizens**. I built RESTful APIs and a JWT-based role management system, and optimized MongoDB aggregation pipelines to cut query latency by **40%**. *(Node.js, MongoDB)*
- **Payconz:** a Flask currency-conversion API for 5 currencies with PostgreSQL, for real-time multi-currency payroll and monthly currency-history reports.
- Deployed services on Linux cloud servers and coordinated releases with clients.

## Graduate Research Assistant · Oklahoma State University

*Stillwater, Oklahoma · Jan 2024 – May 2026*

- Built an LLM agent system that lets people request, check, download, and verify zero-knowledge proofs in plain language through **8 custom MCP tools**. Server-side checks raised task completion from **70% to 93%** across 6,000+ test runs on 3 model families. *(LangGraph, FastMCP, Flask, Redis, PostgreSQL, Docker)*
- Built a DDoS detection and mitigation system for Kubernetes and Istio that runs as a single monitoring pod, with per-service ML models (**94.0–97.8% accuracy**), automatic traffic rerouting, and parallel inference **2.27× faster** than one central model.
- Contributed a merged pull request to the open-source [CoSMeTIC](https://github.com/disys-lab/cosmetic) zkSNARK framework, including a fix for a bug that reported every valid KS and LRT proof as failed.

## AI Instructor · NSF Research Experiences for Teachers

*Oklahoma State University · May 2025 – Aug 2025*

- Taught 10 K–12 teachers Python, machine learning, and Transformers through hands-on tutorials, guided their projects, and designed a Python-to-LLM curriculum.

## Undergraduate Research Assistant · BRAC University

*Dhaka, Bangladesh · Oct 2020 – Jan 2023*

- Designed an image compression module and built a cloud storage and retrieval framework that cut user waiting time by up to **54%** and image size by up to **27%**, published in *IEEE Transactions on Cloud Computing* (corresponding author).

# Featured Projects

## LLM Agent for Zero-Knowledge Proofs

*Python · LangGraph · FastMCP · Flask · Redis · PostgreSQL · Docker* · [**Code**](https://github.com/disys-lab/Skeptical-MCP-For-zkSNARKs) · [**Paper**](https://github.com/disys-lab/Skeptical-MCP-For-zkSNARKs/blob/main/manuscript/Natural-Language-ZK-Verification-via-Skeptical-MCP-Tools.pdf)

A chat assistant that lets non-experts run a zero-knowledge proof system (CoSMeTIC) in plain language: a LangGraph ReAct agent calls 8 custom MCP tools, and Redis and PostgreSQL keep session and user state. LLMs often leave out or invent the exact values these tools need, so I designed 20 server-side checks that complete or override what the model sends before any tool runs.

- An interceptor replaces any user ID the model invents with the real session identity.
- A "plausible default" inside one tool sent **198 status checks to the wrong backend**; a server-side override removed all 198.
- I evaluated it with my own 82-query test suite in 5 configurations and released the code, test suite, and all 6,371 result records, with a script that recomputes every number.

[![System architecture of the LLM agent](/images/skeptical_architecture.png){: .wide-shot}](/images/skeptical_architecture.png)
*How it works: every tool call from the LLM agent passes through an interceptor that replaces any identity the model invents, and the MCP server checks the request against stored state before calling the provers. Labels such as A3 and B2–B7 are design decisions from the paper, for example A3 (server-side identity) and B4–B6 (finding the right job, proof type, and prover from stored state).*

## DDoS Defense for Kubernetes Service Meshes

*Python · scikit-learn · Kubernetes · Istio · Envoy · Prometheus* · [**Prototype code**](https://github.com/nazrulhuda/AI-Driven-Anomaly-Detector-and-mitigation-as-a-service) · [**Paper**](https://drive.google.com/file/d/1KdqIUXU8p5YX9Xib-yazjfmLLQQOJWKe/view?usp=sharing)

A flood of requests to one microservice can bring a whole app down, and service meshes like Istio only offer fixed rules set by hand. I built a framework that runs as a single monitoring pod, needs no changes to application code, detects attacks per service, and moves traffic away automatically.

[![How the DDoS detection and rerouting framework works](/images/ddos_architecture.jpg){: .side-shot}](/images/ddos_architecture.jpg)

- Reads each service's traffic from its Envoy sidecar's Prometheus endpoint.
- Per-service classifiers (Random Forest, Gradient Boosting, SVM, Decision Tree) trained on 4,705 labeled traffic windows reach **94.0–97.8% accuracy**, with an Isolation Forest fallback for new services.
- Patches Istio DestinationRule and VirtualService resources through the Kubernetes API to move traffic to backup versions, then restores normal routing after a cooldown.
- Parallel inference takes **37.4 ms instead of 84.8 ms** per detection cycle on a 12-pod testbed.

<div style="clear: both;"></div>

## FwdStar, a Freight Marketplace

*Next.js · TypeScript · FastAPI · PostgreSQL/PostGIS · Docker · 2026–present (MVP)* · [**Details**](/projects/)

A multi-sided marketplace for shippers, brokers, and carriers in Bangladesh, where I am the technical lead and sole architect. I wrote the technical specification from the client's needs and built it in nine phases, from phone-first sign-up to shipment tracking.

- FastAPI backend with **50+ documented REST endpoints** and a Next.js frontend in English and Bengali.
- Supabase PostgreSQL with PostGIS (20+ tables), state machines with optimistic locking, and `SELECT FOR UPDATE` so a load is never awarded twice.
- JWT verification, HTTP-only cookie sessions, CSRF protection, OTP with rate limiting, and audit logging.

More projects, including a LangChain + MCP chatbot and a license-plate reader, are on the [Projects](/projects/) page.

# Education

- **M.S. in Computer Science**, Oklahoma State University · Jan 2024 – May 2026 · GPA 3.82/4.0
- **B.S. in Computer Science**, BRAC University · May 2018 – May 2022

# Publications

My papers include a corresponding-author paper in *IEEE Transactions on Cloud Computing* and a first-author paper on the LLM agent above, under review at IEEE BigData 2026. [All publications](/publications/)

# Outside Work

I am the founding captain of **Lagaan**, a cricket team in Stillwater, Oklahoma, which has won two trophies ([Hobbies](/hobbies/)).
