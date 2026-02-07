# FieldVoice Pro — Admin Dashboard

A multi-page admin dashboard for **FieldVoice Pro**, a voice-powered construction field reporting system for DOT-compliant daily reports.

## 🏗️ Overview

This dashboard is the **office/admin side** that complements the FieldVoice Pro field app. While RPR inspectors use the mobile app on construction sites to capture daily reports via voice, text, or hybrid input, project managers and office staff use this dashboard to:

- Monitor all active projects from a single command center
- Review and approve AI-refined field reports
- Communicate with field inspectors in real-time
- Track material deliveries and shipments
- Manage project calendars and scheduling
- View and organize geotagged field photos
- Leverage AI insights for project intelligence
- Manage field users and their report history

## 📱 Pages

| Page | Description |
|------|-------------|
| **Command Center** (`index.html`) | Main dashboard with KPIs, live activity feed, weather, map, and quick actions |
| **Report Center** (`reports.html`) | All field reports with filters, AI side-by-side comparison, and PDF export |
| **Communications** (`messages.html`) | Real-time messaging with field inspectors, organized by project |
| **Deliveries** (`deliveries.html`) | Material delivery tracking with timeline and status management |
| **Calendar** (`calendar.html`) | Job calendar with color-coded events for pours, inspections, deliveries |
| **Photos** (`photos.html`) | Geotagged photo management with grid and map views |
| **AI Insights** (`ai-insights.html`) | AI command center with knowledge base, quality scores, and conversational AI |
| **Users** (`users.html`) | Field user management with report history and performance stats |

## 🎨 Design Language

Matches the FieldVoice Pro field app's DOT/construction theme:
- **Colors:** dot-navy (#0a1628), dot-blue (#1e3a5f), dot-orange (#ea580c), dot-yellow (#f59e0b), safety-green (#16a34a)
- **Safety stripe pattern** at the top of every page
- **Dark mode** throughout for extended use
- Professional, data-dense but clean layout

## 🔧 Technical Details

- **No build step required** — pure HTML/CSS/JS
- **Tailwind CSS** via CDN for styling
- **Font Awesome 6.4** for icons
- **Leaflet.js** for maps
- **Self-contained pages** — each HTML file works independently
- **Responsive** but desktop-first

## 📋 Demo Data

All data is **mock/demo** data based on real construction projects at the New Orleans airport (MSY):

### Projects
- North-South Connector Road Phase 2
- CBIS Expansion  
- Express Shuttle Connector Road

### Contractors
- Hunt Gibbs Boh Metro (prime contractor)
- Kass Brothers (storm drain)
- Boh Bros (concrete)
- Frischhertz Electric
- Peterson Plumbing

### Inspectors
- Jackson Koerner — RPR, Ad Videre
- Justin Cain — RPR, Burns & McDonnell
- Andrew Stiebing — RPR, Burns & McDonnell

## 🚀 Getting Started

Just open `index.html` in a browser. No server required.

Or serve locally:
```bash
python3 -m http.server 8080
# Open http://localhost:8080
```

## 📡 Architecture Context

The full FieldVoice Pro system includes:
- **Field App** (v6.9) — Mobile app for RPR inspectors
- **Admin Dashboard** (this repo) — Desktop dashboard for office staff
- **Supabase Backend** — Shared database (project ref: wejwhplqnhciyxbinivx)
- **n8n Workflows** — AI refinement pipeline (fieldvoice-refine-v6.6, fieldvoice-project-extractor-6.5)

This dashboard is currently a **demo/prototype** with mock data. Future versions will connect to the live Supabase backend.

## 📄 License

MIT
