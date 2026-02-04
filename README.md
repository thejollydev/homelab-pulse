# Homelab Pulse

> Real-time monitoring dashboard for homelab infrastructure

[![Status](https://img.shields.io/badge/status-in%20development-yellow)](https://github.com/thejollydev/homelab-pulse)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## 🎯 Project Overview

A modern, responsive dashboard for monitoring homelab infrastructure in real-time. Provides visibility into system metrics, service health, and container status with beautiful visualizations.

**🚧 Currently in active development - check back soon!**

## ✨ Features (Planned)

- 📊 **Real-Time Metrics** - Live system and service metrics via WebSocket
- 🎨 **Beautiful UI** - Modern, responsive design with dark mode
- 🐳 **Container Management** - Monitor and manage Docker containers
- 🚨 **Alert Display** - Visual alerts from Grafana/Prometheus
- 📈 **Historical Charts** - Interactive time-series visualizations
- 🖥️ **Service Status** - Health checks for all homelab services

## 🛠️ Tech Stack

**Frontend:**
- React 18 (with Hooks)
- TypeScript
- Material-UI / shadcn/ui
- Recharts (data visualization)
- WebSocket client
- Tailwind CSS
- Vite (build tool)

**Backend:**
- FastAPI (REST API + WebSocket server)
- Prometheus (metrics source)
- Docker API integration
- Real-time metric streaming

## 🏗️ Architecture
```
┌──────────────────┐
│  React Frontend  │ ← WebSocket client
└────────┬─────────┘
         │ HTTP + WS
┌────────▼─────────┐
│  FastAPI Backend │ ← WebSocket server
└────────┬─────────┘
         │ PromQL
┌────────▼─────────┐
│   Prometheus     │ ← Metrics collection
└──────────────────┘
```

## 🚀 Quick Start (Coming Soon)
```bash
# Clone the repository
git clone https://github.com/thejollydev/homelab-pulse.git
cd homelab-pulse

# Start backend
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

# Start frontend (separate terminal)
cd frontend
npm install
npm run dev
```

## 📱 Screenshots

*Coming soon - Dashboard mockups and live screenshots*

## 🎨 Design Principles

- **Fast** - Sub-second load times, optimized bundle
- **Responsive** - Mobile, tablet, and desktop support
- **Accessible** - WCAG AA compliance
- **Modern** - Clean, professional aesthetics

## 📊 Metrics Displayed

- CPU usage (per core and aggregate)
- Memory utilization with trends
- Disk space and I/O
- Network traffic
- Service uptime and response times
- Container resource usage
- GPU metrics (for LLM inference)

## 🔌 WebSocket Integration

Real-time updates without polling:
- Automatic reconnection with exponential backoff
- Connection state management
- Efficient data streaming
- <1 second latency

## 📝 Blog Post

Read about the development: [Building a Real-Time Monitoring Dashboard](https://soper.dev) *(coming soon)*

## 🔗 Related Projects

- [JollyLab Infrastructure](https://github.com/thejollydev/jolly-lab-infrastructure) - Infrastructure being monitored
- [Career Catalyst](https://github.com/thejollydev/career-catalyst) - Job search platform

## 📫 Contact

- Portfolio: [soper.dev](https://soper.dev)
- LinkedIn: [joseph-soper-dev](https://www.linkedin.com/in/joseph-soper-dev/)
- GitHub: [@thejollydev](https://github.com/thejollydev)
- Email: joseph@soper.dev

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
