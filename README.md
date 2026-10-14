<picture>
  <source media="(max-width: 600px)" srcset="portfolio-hero-mobile.svg" />
  <img src="portfolio-cover.svg" alt="Pakorn Chompunut — AI engineer. Systems builder. Vision, voice and data." width="100%" />
</picture>

<p align="center">
  <a href="#vehicle-vision"><strong>FLAGSHIP WORK</strong></a> &nbsp; / &nbsp;
  <a href="#more-things-i-build">MORE PROJECTS</a> &nbsp; / &nbsp;
  <a href="#recognition-along-the-way"><strong>RECOGNITION</strong></a> &nbsp; / &nbsp;
  <a href="#a-little-about-me">ABOUT ME</a> &nbsp; / &nbsp;
  <a href="mailto:pakorn.c@ntplc.co.th">LET'S TALK ↗</a>
</p>

<p align="center">
  <a href="https://github.com/pakornc2534"><img src="https://img.shields.io/badge/GitHub-pakornc2534-171B20?style=for-the-badge&amp;logo=github&amp;logoColor=F3F0E8" alt="GitHub: pakornc2534" /></a>
  <a href="mailto:pakorn.c@ntplc.co.th"><img src="https://img.shields.io/badge/Email-Let%27s_Talk-FF683B?style=for-the-badge&amp;logo=gmail&amp;logoColor=171B20" alt="Email Pakorn" /></a>
</p>

### สวัสดีครับ, I'm Pakorn.

An **AI engineer and software builder at National Telecom PLC.**, with a background in enterprise data systems since 2014. I work across **computer vision, real-time voice agents, and full-stack applications** — from preparing the data to making the system usable.

My current deep dive: **teaching AI to recognize vehicles in real CCTV footage**, where a new camera angle can change everything.

## Vehicle Vision

<picture>
  <source media="(max-width: 600px)" srcset="vehicle-vision-mobile.svg" />
  <img src="vehicle-vision.svg" alt="Vehicle Vision — deployed in Ang Sila and Don Hua Lo, Chonburi. 1,042 reviewed images and 20 cameras in evaluation." width="100%" />
</picture>

**DEPLOYED IN CHONBURI · Ang Sila & Don Hua Lo**  
ใช้งานจริงในจังหวัดชลบุรี — อ่างศิลาและดอนหัวฬ่อ

### The hard part starts when the camera changes.

Small crops. Unfamiliar angles. Similar-looking brands. I work on the **model and data side** of Vehicle Vision: developing vehicle-brand and color classification, reviewing labels, testing across cameras, and preparing model packages for the deployment team targeting **NVIDIA Jetson AGX Orin**.

**From a hackathon contribution to real-world deployment in Chonburi.** The work has progressed from MobileNetV3 to MobileNetV4, with human-review tools, duplicate screening, per-camera evaluation, and controlled experiments on difficult vehicle classes.

<table>
<tr>
<td width="33%" align="center"><h3>81.29%</h3><strong>Vehicle brand</strong><br /><sub>847 / 1,042 images</sub></td>
<td width="33%" align="center"><h3>88.29%</h3><strong>Vehicle color</strong><br /><sub>920 / 1,042 images</sub></td>
<td width="33%" align="center"><h3>20 cameras</h3><strong>Same-image comparison</strong><br /><sub>Human-reviewed reference labels</sub></td>
</tr>
</table>

<sub>MobileNetV4 v010A · 12 Oct 2026 evaluation · image-level top-1, all 1,042 available vehicle images, no confidence filtering. Brand accuracy was 48.75% for the evaluated V3 checkpoint on these same images. This is an evaluation result, not a claim of live-system accuracy or Jetson speed.</sub>

**What I bring to the work**

- **Data that can be checked:** AI-assisted labeling with human review, duplicate audits, and explicit train/dev/evaluation boundaries.
- **Experiments that explain the tradeoffs:** V3/V4 comparisons, frozen-encoder trials, targeted data additions, and reviews of which brands improve or regress.
- **A practical handoff:** checkpoints, class maps, preprocessing, inference configuration, and evidence for the deployment team.

**Latest · 14 Oct 2026** — Continued model improvements for the deployed Vehicle Vision system, including Formula C. On the reused, AI-labeled development set, brand accuracy is **89.00% (704/791)** and color accuracy is **89.43% (770/861)**. Fresh-data validation remains the next test; Nissan regression is a known tradeoff.

**[Read the engineering case study →](VEHICLE_VISION.md)**

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&amp;logo=python&amp;logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&amp;logo=pytorch&amp;logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/Computer_Vision-171B20?style=for-the-badge" alt="Computer Vision" />
  <img src="https://img.shields.io/badge/NVIDIA_Jetson-76B900?style=for-the-badge&amp;logo=nvidia&amp;logoColor=white" alt="NVIDIA Jetson" />
</p>

## More things I build

<a href="https://github.com/pakornc2534/chanthaburi-ai-guide"><img src="tripchan.svg" alt="TripChan — bilingual AI travel guide for Chanthaburi" width="100%" /></a>

### An AI guide with local knowledge.

**TripChan** helps people explore Chanthaburi through Thai/English chat grounded in a **49-place catalog**, structured 1–3 day itineraries, and a check-in/rewards POC.

<p>
<img src="https://img.shields.io/badge/Agentic%20RAG-24534B?style=flat-square" alt="Agentic RAG" />
<img src="https://img.shields.io/badge/React-24534B?style=flat-square" alt="React" />
<img src="https://img.shields.io/badge/TypeScript-24534B?style=flat-square" alt="TypeScript" />
<img src="https://img.shields.io/badge/Supabase-24534B?style=flat-square" alt="Supabase" />
</p>

**[Explore TripChan ↗](https://github.com/pakornc2534/chanthaburi-ai-guide)**




<a href="https://github.com/pakornc2534/guardian-thai-ai"><img src="eldercare.svg" alt="ElderCare Guardian — privacy-first care workflow prototype" width="100%" /></a>

### Turn risk signals into care workflows.

**ElderCare Guardian** explores camera-free monitoring, explainable risk signals, escalation, and Thai voicebot outreach. An interactive product prototype using **simulated sensors and calls**.

<p>
<img src="https://img.shields.io/badge/React-524465?style=flat-square" alt="React" />
<img src="https://img.shields.io/badge/TypeScript-524465?style=flat-square" alt="TypeScript" />
<img src="https://img.shields.io/badge/Recharts-524465?style=flat-square" alt="Recharts" />
<img src="https://img.shields.io/badge/Product%20prototyping-524465?style=flat-square" alt="Product prototyping" />
</p>

**[Explore Guardian ↗](https://github.com/pakornc2534/guardian-thai-ai)**

**Also in my workshop**

- **[DataOps Pipeline ↗](https://github.com/pakornc2534/dataops-foundation-jenkins-new)** — loan CSV → cleaning → fact/dimension tables → SQL Server, with Python tests and Jenkins orchestration.
- **REDACTRA** — co-developed local-first privacy workflows for vendor assessment, DPA, risk, and DPIA; human review before data leaves the system.
- **Prompy / NT AIoT Smart Home** — coached Team Prompt on Thai voice control, Home Assistant/Tuya, and vision/audio sensing.
- **Real-time multimodal agents** — connecting STT → LLM → TTS through LiveKit / WebRTC.

## Recognition along the way

**Ideas built. Work recognized.** Six recognitions across AI, data privacy, and real-world applications — 2025–2026.

<picture>
  <source media="(max-width: 600px)" srcset="recognition-phone.svg" />
  <img src="recognition.svg" alt="2026: Bronze Medal — Super AI Engineer Season 6, Vehicle Vision; Popular Vote — PDPA Hackathon, REDACTRA; Honorable Mention — OpenAI × AIAT, Life Guardian; Finalist — Dictionary Reimagined. 2025: Winner — NT Big Idea, AI Service Solution; First Runner-up — NT Agentic AI Hackathon, Real-Time Multimodal AI Agents." width="100%" />
</picture>

## A little about me

**Build → test → explain → improve.** That's the part of engineering I enjoy: turning an idea into something people can inspect, use, and make better.

At **National Telecom**, I've worked on enterprise CRM pipelines, customer information systems, and interactive applications since 2014. Since 2024, I've also taught **Generative AI, data storytelling, and UX/UI** at National Telecom Academy.

> ผมชอบงานที่ได้ลงมือทั้งข้อมูล โมเดล และระบบ — แล้วอธิบายให้คนใช้และทีมที่รับช่วงต่อเข้าใจได้จริง

### My tech stack

**AI & REAL-TIME AGENTS**

<p>
  <img src="https://img.shields.io/badge/Python-171B20?style=for-the-badge&amp;logo=python&amp;logoColor=F3F0E8" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-171B20?style=for-the-badge&amp;logo=pytorch&amp;logoColor=F3F0E8" alt="PyTorch" />
  <img src="https://img.shields.io/badge/LangChain-171B20?style=for-the-badge&amp;logo=langchain&amp;logoColor=F3F0E8" alt="LangChain" />
  <img src="https://img.shields.io/badge/LangFlow-171B20?style=for-the-badge" alt="LangFlow" />
  <img src="https://img.shields.io/badge/LiveKit%20%2F%20WebRTC-171B20?style=for-the-badge" alt="LiveKit / WebRTC" />
  <img src="https://img.shields.io/badge/n8n-171B20?style=for-the-badge&amp;logo=n8n&amp;logoColor=F3F0E8" alt="n8n" />
  <img src="https://img.shields.io/badge/MCP-171B20?style=for-the-badge" alt="MCP" />
</p>

**FULL-STACK DEVELOPMENT**

<p>
  <img src="https://img.shields.io/badge/ASP.NET-303840?style=for-the-badge&amp;logo=dotnet&amp;logoColor=F3F0E8" alt="ASP.NET" />
  <img src="https://img.shields.io/badge/Next.js-303840?style=for-the-badge&amp;logo=nextdotjs&amp;logoColor=F3F0E8" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-303840?style=for-the-badge&amp;logo=react&amp;logoColor=F3F0E8" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-303840?style=for-the-badge&amp;logo=typescript&amp;logoColor=F3F0E8" alt="TypeScript" />
</p>

**DATA ENGINEERING & STORAGE**

<p>
  <img src="https://img.shields.io/badge/SQL%20Server-24534B?style=for-the-badge" alt="SQL Server" />
  <img src="https://img.shields.io/badge/SSIS-24534B?style=for-the-badge" alt="SSIS" />
  <img src="https://img.shields.io/badge/Apache%20Spark-24534B?style=for-the-badge&amp;logo=apachespark&amp;logoColor=F3F0E8" alt="Apache Spark" />
  <img src="https://img.shields.io/badge/PySpark-24534B?style=for-the-badge" alt="PySpark" />
  <img src="https://img.shields.io/badge/Apache%20Kafka-24534B?style=for-the-badge&amp;logo=apachekafka&amp;logoColor=F3F0E8" alt="Apache Kafka" />
  <img src="https://img.shields.io/badge/Qdrant-24534B?style=for-the-badge&amp;logo=qdrant&amp;logoColor=F3F0E8" alt="Qdrant" />
</p>

**DATA VISUALIZATION**

<p>
  <img src="https://img.shields.io/badge/Power%20BI-524465?style=for-the-badge" alt="Power BI" />
  <img src="https://img.shields.io/badge/Tableau-524465?style=for-the-badge" alt="Tableau" />
  <img src="https://img.shields.io/badge/Data%20Storytelling-524465?style=for-the-badge" alt="Data Storytelling" />
</p>

**DEPLOYMENT & COMPUTE**

<p>
  <img src="https://img.shields.io/badge/Docker-171B20?style=for-the-badge&amp;logo=docker&amp;logoColor=F3F0E8" alt="Docker" />
  <img src="https://img.shields.io/badge/Git-171B20?style=for-the-badge&amp;logo=git&amp;logoColor=F3F0E8" alt="Git" />
  <img src="https://img.shields.io/badge/CI%2FCD-171B20?style=for-the-badge" alt="CI/CD" />
  <img src="https://img.shields.io/badge/NVIDIA%20Jetson-171B20?style=for-the-badge&amp;logo=nvidia&amp;logoColor=F3F0E8" alt="NVIDIA Jetson" />
  <img src="https://img.shields.io/badge/HPC%20%2F%20Slurm-171B20?style=for-the-badge" alt="HPC / Slurm" />
</p>

### Certifications & learning

<p>
  <img src="https://img.shields.io/badge/Huawei%20Cloud%20%7C%20HCCDA--AI%20Developer-FF683B?style=for-the-badge&amp;logo=huawei&amp;logoColor=171B20" alt="Huawei Cloud | HCCDA-AI Developer" />
  <img src="https://img.shields.io/badge/AIAT%20%7C%20Super%20AI%20Engineer%20S6-24534B?style=for-the-badge" alt="AIAT | Super AI Engineer S6" />
  <img src="https://img.shields.io/badge/English%20%7C%20TOEIC%20635-524465?style=for-the-badge" alt="English | TOEIC 635" />
</p>

<details>
<summary><strong>Education & credentials</strong></summary>

MBA — Ramkhamhaeng University · B.Sc. Information Technology — Rangsit University  
HCCDA-AI Developer — Huawei Cloud · Super AI Engineer Season 6 — AIAT  
Thai · English (TOEIC 635)

</details>

---

### Have a real-world AI problem in mind?

I'm interested in conversations about **computer vision, real-time agents, data engineering, and making AI useful in practice**.

**[Let's talk ↗](mailto:pakorn.c@ntplc.co.th)** &nbsp; · &nbsp; **[Browse my repositories ↗](https://github.com/pakornc2534?tab=repositories)**

<sub>Pakorn Chompunut · ภากร ชมภูนุช · Bangkok, Thailand</sub>
