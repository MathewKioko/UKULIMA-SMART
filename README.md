UKULIMA SMART

UKULIMA SMART is an AI-assisted smart agriculture platform focused on **early crop disease detection**, **decision support**, and **data-driven farm management** for smallholder and large-scale farmers.

The system combines **computer vision**, **real-time data**, and **domain-specific agricultural knowledge** to help farmers detect issues early, reduce losses, and improve yields.

Live Demo: https://ukulimasmart.vercel.app



 Problem Statement

Farmers—especially smallholder farmers—often detect crop diseases too late due to:

* Limited access to agricultural experts
* Lack of timely diagnostic tools
* Poor integration of weather, disease, and crop data
* High cost of professional farm monitoring

Late detection leads to reduced yields, increased pesticide usage, and financial loss.


Solution Overview

UKULIMA SMART provides a *mobile-first, AI-powered decision support system** that enables farmers to:

* Detect crop diseases using images
* Receive treatment recommendations
* Track plant health over time
* Access weather-driven farming insights
* Connect with experts and farming communities

The platform is designed to be scalable, extensible, and region-aware, with a focus on African farming contexts.


Core Features

 AI & Decision Support

* Image-based crop disease detection using CNN models
* Severity classification and confidence scoring
* Treatment and prevention recommendations

Farm Intelligence

* Real-time and forecasted weather insights
* Crop health history and timelines
* Yield prediction (ML-based, experimental)

Platform Capabilities

* Authentication and user management
* Subscription plans with M-Pesa payments
* Community discussion forums
* Educational content and tutorials

---

System Architecture

```
Client (Web / Mobile)
        |
        v
Frontend (React + TypeScript)
        |
        v
API Layer (Supabase REST / Realtime)
        |
        +------------------+
        |                  |
        v                  v
AI/ML Services        PostgreSQL Database
(TensorFlow/PyTorch) (Users, Crops, Images,
                       Predictions, Payments)
        |
        v
External Services
(Weather APIs, M-Pesa)
```

 Design Principles

* Backend as the source of truth
* Stateless frontend
* AI services isolated from core business logic
* Clear separation between data ingestion and inference

---

Tech Stack

Frontend

* React
* TypeScript
* Tailwind CSS
* Shadcn UI

Backend & Data

* Supabase (PostgreSQL + Auth + Realtime)
* REST APIs
* Role-based access control

AI / ML

* TensorFlow / PyTorch
* CNN-based image classifiers
* Model inference via API layer

Cloud & DevOps

* Vercel (Frontend hosting)
* Docker (model experimentation)
* AWS (planned for model serving)

Integrations

* M-Pesa Payments
* Weather APIs
* (Planned) Drone imagery ingestion


Disease Detection Flow

1. User captures or uploads a crop image
2. Image is sent to the inference service
3. ML model performs classification
4. Disease type and severity are returned
5. System generates treatment guidance
6. Result is stored for historical tracking

---

Installation & Local Setup
 Prerequisites

* Node.js 18+
* Supabase account
* API keys for weather and payments (optional)

### Setup

```bash
git clone https://github.com/MathewKioko/UKULIMA-SMART.git
cd UKULIMA-SMART
npm install
cp .env.example .env
npm run dev
```

### Environment Variables

```env
VITE_SUPABASE_URL=
VITE_SUPABASE_ANON_KEY=
VITE_WEATHER_API_KEY=
VITE_MPESA_CONSUMER_KEY=
VITE_MPESA_CONSUMER_SECRET=
```


Limitations (Current)

* Model accuracy depends on image quality
* Limited crop and disease coverage
* No offline support
* Experimental yield prediction models

These are known constraints and part of the roadmap.


Roadmap

* Mobile application (React Native)
* Offline-first disease detection
* Multilingual support (Swahili first)
* IoT soil and irrigation sensor integration
* Advanced analytics dashboards
* Supply-chain and produce traceability

Contribution Guidelines

Contributions are welcome in the following areas:

* Model training and evaluation
* Dataset curation
* Frontend UX improvements
* Documentation
* Agricultural domain expertise

Please open an issue before submitting major changes.


 License

MIT License. See [LICENSE](LICENSE).



Author

**Mathew Kioko**
Software Engineer | Backend & Systems | Applied AI
GitHub: [https://github.com/MathewKioko](https://github.com/MathewKioko)


