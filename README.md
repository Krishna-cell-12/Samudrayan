# Samudrayan — E-DNA Voyage

**AI-Driven Deep Sea eDNA Analysis Platform**

Unveiling the ocean's hidden biodiversity through an AI-powered environmental DNA (eDNA) analysis pipeline for discovering novel marine species in the deep ocean.

---
<img width="1885" height="917" alt="image" src="https://github.com/user-attachments/assets/18af84db-ee8d-41dc-b37b-8161ffdf5995" />


## Overview

Samudrayan (e-DNA Voyage) is a modern web application designed to support marine biodiversity research. It enables researchers to upload eDNA samples, run AI-powered analyses, visualize results through phylogenetic trees and geographic dashboards, and manage collaborative research projects—all within a single, intuitive interface.

The platform addresses key challenges in deep-sea genomics: limited genetic databases, lengthy processing times, and the difficulty of identifying novel taxa. By combining structured data management with interactive visualizations, it aims to accelerate the discovery of undiscovered marine species.

---

## Features

### Core Functionality

| Feature | Description |
|---------|-------------|
| **Sample Upload** | Drag-and-drop eDNA file upload with progress tracking, geolocation tagging, and metadata capture |
| **Analysis Pipeline** | Simulated AI-driven analysis with species identification, confidence scoring, and novel taxa detection |
| **Results Visualization** | Phylogenetic tree views, zone-grid exploration, and taxonomic aggregation (phylum/class levels) |
| **Global Dashboard** | Interactive map showing biodiversity data across major deep-sea locations (e.g., Mariana Trench, Puerto Rico Trench, Japan Trench) |
| **Project Management** | Create and manage research projects with collaborators, date ranges, file associations, and tags |
| **User Profiles** | Profile management with editable user information |
| **Authentication** | Sign-in and registration flows for authenticated access |

### Technical Capabilities

- **State Management**: React Context for Analysis, Projects, and User data with `localStorage` persistence
- **Data Visualization**: Recharts, phylogenetic trees, geographic maps, and interactive zone grids
- **Form Handling**: React Hook Form with Zod validation
- **API-Ready**: TanStack Query for server state management and future backend integration
- **Responsive UI**: Mobile-friendly layout built with Tailwind CSS and shadcn/ui

---

## Technology Stack

| Category | Technologies |
|----------|--------------|
| **Framework** | React 18, TypeScript |
| **Build Tool** | Vite 5 |
| **Styling** | Tailwind CSS, Tailwind Typography |
| **UI Components** | shadcn/ui, Radix UI primitives |
| **Routing** | React Router v6 |
| **Data Fetching** | TanStack React Query |
| **Forms & Validation** | React Hook Form, Zod, @hookform/resolvers |
| **Charts & Visualization** | Recharts |
| **3D Graphics** | Spline (react-spline) |
| **Icons** | Lucide React |
| **Date Handling** | date-fns, react-day-picker |

---

## Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── ui/              # shadcn/ui base components
│   ├── AbyssBackground.tsx
│   ├── AuthModal.tsx
│   ├── CollaboratorModal.tsx
│   ├── DataVisualization.tsx
│   ├── GlobalMap.tsx
│   ├── Navigation.tsx
│   ├── PhylogeneticTree.tsx
│   ├── ProjectDetailsModal.tsx
│   ├── ProjectResultsModal.tsx
│   ├── SpeciesDiscovery.tsx
│   └── ZoneGrid.tsx
├── contexts/            # React Context providers
│   ├── AnalysisContext.tsx
│   ├── ProjectContext.tsx
│   └── UserContext.tsx
├── hooks/               # Custom React hooks
├── lib/                 # Utility functions
├── pages/               # Route-level pages
│   ├── Home.tsx
│   ├── Upload.tsx
│   ├── Results.tsx
│   ├── Dashboard.tsx
│   ├── Projects.tsx
│   ├── Profile.tsx
│   └── NotFound.tsx
└── services/            # External service integrations
    ├── emailService.ts
    └── locationService.ts
```

---

## Getting Started

### Prerequisites

- **Node.js** 18+ (recommended: [install via nvm](https://github.com/nvm-sh/nvm#installing-and-updating))
- **npm** or **Bun**

### Installation

```bash
# Clone the repository
git clone <YOUR_GIT_URL>
cd e-dna-voyage

# Install dependencies
npm install

# Start the development server
npm run dev
```

The application will be available at `http://localhost:5173` (or the port shown in the terminal).

### Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server with hot module replacement |
| `npm run build` | Production build |
| `npm run build:dev` | Development mode build |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint |

---

## Application Routes

| Path | Page | Description |
|------|------|-------------|
| `/` | Home | Landing page with product overview and value proposition |
| `/upload` | Upload | eDNA sample upload and analysis initiation |
| `/results` | Results | Analysis results, phylogenetic trees, and zone exploration |
| `/dashboard` | Dashboard | Global ocean biodiversity dashboard and map |
| `/projects` | Projects | Project management and collaboration |
| `/profile` | Profile | User profile and settings |

---

## Data Persistence

Analysis data (uploaded files and results) is persisted in the browser's `localStorage` under the keys:

- `e-dna-uploaded-files`
- `e-dna-analysis-results`

This enables session continuity during development. For production, integrate with a backend API and replace or extend the context implementations.

---

## Development Notes

- **ESLint** is configured for code quality; run `npm run lint` before committing.
- **TypeScript** is used throughout; ensure type definitions are maintained.
- UI components follow shadcn/ui conventions and use Tailwind for styling.

---

## License

Private. All rights reserved.

---

## Acknowledgments

Built for marine biodiversity research, inspired by deep-sea exploration and environmental DNA science. Samudrayan references India's pioneering manned submersible mission for deep-ocean research.
