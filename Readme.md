<div align="center">
# Rayane Aboud

**Backend & AI Engineer** · Grenoble, France 🇫🇷 · from Algiers 🇩🇿

*M2 Computer Science @ Université Grenoble Alpes · State Engineer, ESI Algiers (16.27/20, Très Bien) · MedCCAI 2025*

[![Portfolio](https://img.shields.io/badge/Portfolio-rayaneaboud.dev-111?style=flat-square&logo=googlechrome&logoColor=white)](https://rayaneaboud.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rayane-aboud-611ab91a5/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:rayane.aboud02@gmail.com)
[![Discord](https://img.shields.io/badge/Discord-7289DA?style=flat-square&logo=discord&logoColor=white)](https://discord.com/users/rayane_aboud)

</div>

---

I'm a backend and AI engineer. I like building systems that keep working in production, whether it's a
Rust service, an MLOps pipeline or an app that uses an LLM. I've spent two years doing this for a large
marketplace, a government platform and a few startups.

📌 **I'm looking for an end-of-studies internship (PFE) in backend or AI, starting January 2027**, in
Grenoble or remote. It would be 2 days at school and 3 days at the company at first, then full time.

What I work on most: backend and distributed systems, performance, MLOps and edge AI, and LLM integration.

---

### What I've done

- At **Ouedkniss**, Algeria's biggest marketplace (more than 2 million users a day), I rewrote the service
  that brings in the most revenue from PHP to Rust. Latency went down by **60%** and the number of pods
  went from **40 to 13**. I also built an in-memory cache that answers in under a millisecond.
- At **GACA / Avimed**, on an e-services platform for the Saudi civil aviation authority, I migrated the
  app from Java 8 and JSP to Java 17, Spring and React without any downtime, and redesigned more than 40
  REST endpoints.
- At **Namla**, an edge cloud platform, I built energy forecasting with LSTM models (R² between 0.93 and
  0.99) and the whole MLOps pipeline around it: training in the cloud, inference at the edge, and
  automatic retraining. Compared with a cloud-only design, latency went down by **68%** and the data sent
  to the cloud by **90%**.
- At **Aircrop**, an agri-tech startup, I worked as a freelancer on the Python backends (FastAPI, then
  Django) that combine a crop-disease model with an LLM-written health report. The proof of concept helped
  the startup get its official label.
- I co-authored a paper: [Edge AI System for Optimizing Energy Consumption for Smart Buildings](https://www.researchgate.net/publication/392071334_Edge_AI_system_for_optimizing_energy_consumption_for_smart_buildings), MedCCAI 2025.

---

### Projects

| Repo | Description | Stack |
|------|-------------|-------|
| [FacadeLang](https://github.com/Rayane-Aboud/facade-lang) ([try it](https://rayaneaboud.dev/facade-lang/)) | A small typed language for building design. If you mix up two lengths, like a thickness and an inset, the checker catches it before anything gets built. It has a parser, a type checker, a browser playground with a 3D preview and a VS Code extension. | Rust, WebAssembly |
| [Aircrop](https://github.com/Rayane-Aboud/aircrop) | Upload a photo of a crop and get a health check, the weather of that day and a short agronomy report as a PDF. Deployed on Kubernetes. | Python, Django, YOLO, Gemini, React, K8s |
| [Edge-to-cloud smart metering](https://github.com/Rayane-Aboud/microservices) | The platform from my internship at Namla. Energy readings travel from IoT sensors through MQTT and Kafka, the data is sent encrypted to the cloud, models are trained there and then run at the edge. | NestJS, Python, PyTorch, Kafka, NATS, InfluxDB |
| [ifc-graph-twin](https://github.com/Rayane-Aboud/ifc-graph-twin) | A base layer for digital twins. It reads IFC4 building models, turns them into a graph, stores it in Neo4j and lets you query it through an API. | Rust, Neo4j, Axum |
| [tiny_vmm](https://github.com/Rayane-Aboud/tiny_vmm) | A small virtual machine monitor on top of KVM, written to understand how tools like Firecracker work. | Rust, KVM |
| [Distributed Nodes](https://github.com/Rayane-Aboud/distributed-nodes) | A supervisor and worker cluster over plain TCP, with my own handshake so new nodes can join and find each other. | Rust |
| [Sho3la](https://github.com/Rayane-Aboud/neural-networks-cpp) | A small neural network library I'm writing from scratch to understand what happens under the hood of PyTorch. | C++ |
| [AES-CTR with OpenMP](https://github.com/Rayane-Aboud/aes_encrypt_with_parallelization) | AES-128 written by hand, then made faster by encrypting the blocks in parallel. | C, OpenMP |

<sub>School projects: [MPI exercises](https://github.com/Rayane-Aboud/MPI-Introduction) · [tabu search for bin packing](https://github.com/Rayane-Aboud/tabu-search-bin-packing-cpp) · [matrix library](https://github.com/Rayane-Aboud/Basic-matrix-library-using-c-) · [smart irrigation on Arduino](https://github.com/Rayane-Aboud/Irrigation_system) · [DigiShop, a Flask e-commerce site (team project)](https://github.com/Rayane-Aboud/DigiShop)</sub>

---

### Stack

![Rust](https://img.shields.io/badge/Rust-000?style=flat-square&logo=rust&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/C-555?style=flat-square&logo=c&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
<br>
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
<br>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![LLM](https://img.shields.io/badge/LLM_integration-6B4FBB?style=flat-square&logo=openai&logoColor=white)

---

### Stats

<div align="center">

<img width="48%" src="https://github-readme-stats.vercel.app/api?username=Rayane-Aboud&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00C8FF&icon_color=00C8FF&text_color=C9D1D9&include_all_commits=true&count_private=true" />
<img width="48%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rayane-Aboud&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00C8FF&text_color=C9D1D9&langs_count=6" />

</div>

---

<div align="center">
<sub>⭐ from Algiers to Grenoble with 💚 ❤️ 🖤 🤍 · <em>"optimizing systems one microsecond at a time"</em></sub>
</div>
