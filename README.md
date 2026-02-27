# 🛰️ Drishya AI — Satellite-Based Urban Change Detection

> **Detect urban changes from space using Sentinel-2 imagery and Deep Learning**

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Hugging_Face_Spaces-blue)](https://huggingface.co/spaces/prabhs4546/drishya-ai)
[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://tensorflow.org)
[![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=next.js)](https://nextjs.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## 🚀 Live Demo

👉 **[Try it live on Hugging Face Spaces](https://huggingface.co/spaces/prabhs4546/drishya-ai)**

---

## 📌 What It Does

Enter any location worldwide — the AI fetches satellite images from two different time periods and highlights **exactly where changes occurred** (urbanization, deforestation, flooding, etc.)

```
📍 Location ──▶ 🛰️ Sentinel-2 Images ──▶ 🧠 U-Net CNN ──▶ 🎯 Change Map + Stats
```

---

## 🖼️ Project Architecture

| Component | Folder | Tech Stack | What it does |
|---|---|---|---|
| **Frontend** | `Driahya_lens/` | Next.js, React, Leaflet, Gemini AI | Interactive map dashboard with NL queries |
| **Backend** | `Drishya_backend/` | Python, TensorFlow, Gradio, Sentinel Hub | Satellite change detection with U-Net model |

---

## 🔧 Key Features

- 🌍 **Global Coverage** — Enter any city or region name
- 🧠 **U-Net Deep Learning** — Pixel-level change detection
- ☁️ **Cloud-Free Images** — Auto-selects 0% cloud cover satellite images
- 📏 **Zoom Control** — City-Wide, Block-Level, or Zoomed-In views
- 🖼️ **Multiple Resolutions** — 10m, 5m, or 2.5m per pixel
- 🎨 **Visual Overlay** — Red highlights + yellow contours on change areas
- 📊 **Change Statistics** — Percentage of pixels changed
- 🗺️ **Interactive Map** — Leaflet-based map with property heatmaps & climate risk (Frontend)
- 💬 **Gemini AI Queries** — Natural language search like "Show flood-prone areas in Pune" (Frontend)

---

## 🧠 Model Details

| Attribute | Details |
|---|---|
| **Architecture** | U-Net (Semantic Segmentation) |
| **Input** | Concatenated before + after RGB images (128×128) |
| **Output** | Binary change mask (changed / unchanged per pixel) |
| **Framework** | TensorFlow / Keras |
| **Data Source** | Sentinel-2 L2A via Sentinel Hub API |
| **Bands** | B04 (Red), B03 (Green), B02 (Blue) |

---

## 🚀 Tech Stack

| Layer | Technologies |
|---|---|
| **Deep Learning** | TensorFlow, Keras, U-Net |
| **Satellite Data** | Sentinel Hub API, Sentinel-2 L2A |
| **Computer Vision** | OpenCV, NumPy, Pillow |
| **Frontend** | Next.js 15, React 19, TypeScript, Tailwind CSS, Leaflet |
| **AI Integration** | Google Gemini API |
| **Backend** | FastAPI, Gradio, Uvicorn |
| **Geocoding** | Geopy (Nominatim) |
| **Deployment** | Hugging Face Spaces, Vercel |

---

## 🏃 Run Locally

### Backend (Satellite Change Detection)
```bash
cd Drishya_backend
python -m venv venv
venv\Scripts\activate          # Windows
pip install -r requirements.txt

# Add credentials in .env
# CLIENT_ID=your_sentinel_hub_id
# CLIENT_SECRET=your_sentinel_hub_secret

python app.py                  # Opens at http://localhost:7860
```

### Frontend (Map Dashboard)
```bash
cd Driahya_lens
npm install
npm run dev                    # Opens at http://localhost:3000
```

---

## 🔑 API Keys

| Key | Required | Get it from |
|---|---|---|
| `CLIENT_ID` | ✅ Backend | [Sentinel Hub](https://apps.sentinel-hub.com/dashboard/) |
| `CLIENT_SECRET` | ✅ Backend | [Sentinel Hub](https://apps.sentinel-hub.com/dashboard/) |
| `GEMINI_API_KEY` | Optional (Frontend) | [Google AI Studio](https://makersuite.google.com/app/apikey) |

---

## 👨‍💻 Author

**Prabhdeep Singh Narula**

## 📄 License

MIT License
