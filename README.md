<div align="center">

# Manga Studio

### AI-Powered Manga & Manhwa Generator

Create stunning manga illustrations with AI. Design custom manga pages with professional styles, dynamic layouts, and cinematic quality.

[![Frontend](https://img.shields.io/badge/Frontend-Next.js_16-black?style=for-the-badge&logo=next.js)](./frontend)
[![Backend](https://img.shields.io/badge/Backend-NestJS-red?style=for-the-badge&logo=nestjs)](./backend)
[![AI](https://img.shields.io/badge/AI-Gemini-4285F4?style=for-the-badge&logo=google)](https://ai.google.dev/)
[![Live](https://img.shields.io/badge/Live-Demo-amber?style=for-the-badge&logo=vercel)](https://manga-clement-ai.vercel.app)

</div>

---

## Overview

**Manga Studio** is a full-stack web application that empowers creators and artists to generate AI-driven manga/manhwa stories visually. It combines a modern Next.js frontend with a robust NestJS backend, powered by Google Gemini AI for image generation.

## Project Structure

This repository contains two sub-projects managed as **Git submodules**:

| Project | Description | Tech Stack | Link |
|---------|-------------|------------|------|
| [`frontend/`](https://github.com/youngclement/manga-clement-ai) | Next.js web application | Next.js 16, React 19, Tailwind CSS, Zustand, Zod, React Hook Form | [View Repo](https://github.com/youngclement/manga-clement-ai) |
| [`backend/`](https://github.com/youngclement/backend-manga-generator) | NestJS API server | NestJS, MongoDB, Cloudinary, JWT Auth, Google Gemini AI | [View Repo](https://github.com/youngclement/backend-manga-generator) |

## Features

- **AI Manga Generation** - Generate manga/manhwa pages using Google Gemini AI
- **Multiple Art Styles** - Manhwa 3D, Shonen, Seinen, Shoujo, Webtoon, Digital Painting, and more
- **Smart Story Continuation** - AI automatically continues your story across pages
- **Batch Generation** - Generate multiple pages at once (x5, x10, x15)
- **Panel Layouts** - Single panel, multi-panel, dynamic freestyle, action sequence, etc.
- **Character Consistency** - AI maintains character appearance across pages
- **Reference Images** - Upload reference images for style/character guidance
- **Project Management** - Save, load, organize manga projects
- **Community Gallery** - Share and browse public manga projects
- **User Authentication** - Register, login with JWT-based auth
- **Profile Management** - Customize your creator profile
- **Cloud Storage** - Images stored on Cloudinary, projects on MongoDB
- **Responsive Design** - Works on desktop and mobile
- **Export** - Download pages as PNG or PDF

## Quick Start

### Clone with submodules

```bash
git clone --recurse-submodules https://github.com/youngclement/manga-studio.git
cd manga-studio
```

If you already cloned without `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

### Frontend Setup

```bash
cd frontend
pnpm install
cp .env.example .env.local  # Configure environment variables
pnpm dev
```

### Backend Setup

```bash
cd backend
pnpm install
cp .env.example .env  # Configure environment variables
pnpm start:dev
```

### Environment Variables

**Frontend** (`.env.local`):
```env
NEXT_PUBLIC_BACKEND_URL=http://localhost:3000
API_KEY=your-gemini-api-key
```

**Backend** (`.env`):
```env
PORT=3000
MONGODB_URI=your-mongodb-connection-string
API_KEY=your-gemini-api-key
CLOUDINARY_URL=your-cloudinary-url
JWT_SECRET=your-jwt-secret
JWT_REFRESH_SECRET=your-jwt-refresh-secret
FRONTEND_URLS=http://localhost:3001,http://localhost:3000
```

## Tech Stack

### Frontend
- **Framework**: Next.js 16 (App Router)
- **UI**: React 19, Tailwind CSS 4, Radix UI, Framer Motion
- **State**: Zustand
- **Forms**: React Hook Form + Zod validation
- **Notifications**: Sonner

### Backend
- **Framework**: NestJS
- **Database**: MongoDB
- **Storage**: Cloudinary
- **Auth**: JWT (access + refresh tokens)
- **AI**: Google Gemini API
- **Validation**: class-validator, class-transformer

## Architecture

```
manga-studio/
  frontend/          <- Next.js frontend (submodule)
    app/             <- Pages (auth, studio, community, profile)
    components/      <- UI components
    lib/             <- Services, types, utilities
  backend/           <- NestJS backend (submodule)
    src/
      auth/          <- JWT authentication
      generate/      <- AI manga generation
      projects/      <- Project CRUD
      images/        <- Cloudinary image management
      users/         <- User profiles
      services/      <- Gemini AI, MongoDB, Cloudinary
```

## Live Demo

- **Website**: [manga-clement-ai.vercel.app](https://manga-clement-ai.vercel.app)
- **Backend API**: Hosted on Render

## Author

**ClementHoang** ([@youngclement](https://github.com/youngclement))

---

<div align="center">
  <sub>Built with Next.js, NestJS, and Google Gemini AI</sub>
</div>

