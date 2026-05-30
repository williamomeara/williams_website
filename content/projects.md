+++
date = '2026-05-30T12:00:00Z'
draft = false
title = 'Projects'
+++

# Projects

A selection of products and tools I've designed and built — most under [Cú Chulainn Tech](https://cuchulainntech.ie). Status tags reflect each project's real state today.

## AI & Developer Tooling

### iam-legend
A GCP IAM toolbelt for AI agents and CI pipelines. It parses Terraform, ADK Python, and `gcloud` scripts, recommends least-privilege roles using a set-cover algorithm over a catalog of 2,300+ roles and 13,000+ permissions, and posts AI-driven IAM reviews on pull requests to catch permission gaps before `terraform apply` fails. Built for the **Google for Startups AI Agents Challenge 2026**.
`Python · Gemini/Vertex AI · FastAPI · MCP / CLI / GitHub Action`
**Status:** Open source · [GitHub](https://github.com/williamomeara/iam-legend)

### did-i-do-good
An MCP server that ships Claude's plans to GitHub Copilot for adversarial review — Copilot hunts for missing edge cases, architectural problems, and unstated assumptions at maximum reasoning effort, then feeds them back.
`TypeScript · Model Context Protocol · Node.js`
**Status:** Open source · [GitHub](https://github.com/williamomeara/did-i-do-good)

### flutterctl
A CLI and MCP server that drives Flutter programmatically — hot reload, screenshots, widget-tree inspection, logs, and memory profiling — exposing 14 tools so AI agents and CI can control a running Flutter app with zero app modification.
`Dart · Flutter daemon/VM service · MCP`
**Status:** Open source · [GitHub](https://github.com/williamomeara/flutterctl)

### blindfold-env
A CLI and MCP tool that manages `.env` secrets without ever exposing their values to an AI assistant's context window — values are masked, edited atomically, and gated behind permission rules injected into the assistant's settings.
`Python · Click · FastMCP`
**Status:** Open source · [GitHub](https://github.com/williamomeara/blindfold-env)

## Web Platforms & SaaS

### Every Company Ever
A search engine over every Irish registered company (~815k from the CRO register) with AI-enriched descriptions. Combines full-text (BM25) and vector search for hybrid retrieval, supplemented with charity and financial-statement data.
`FastAPI · PostgreSQL + pgvector/ParadeDB · sentence-transformers · LLM enrichment`
**Status:** Live · [everycompanyever.ie](https://everycompanyever.ie)

### TenderMatch
A multi-tenant platform that matches organisations with public tenders, grants, and funding opportunities using a constraint-based matching engine, with subscription billing, scraping/aggregation, and team management.
`Django · React · Google OR-Tools · Celery/Redis · Stripe`
**Status:** Live · [tendermatch.ie](https://tendermatch.ie)

### Student Placement Management Platform
An enterprise platform managing 600+ student work placements across hundreds of providers and tutors. Features a constraint-based allocation engine, four role portals, compliance/document tracking, assessment workflows, and deep institutional integrations (LTI 1.3 for Canvas/Moodle, SIS sync, SSO).
`Django · Google OR-Tools · PostgreSQL + pgvector · LTI 1.3 · Azure AD SSO`
**Status:** Client project (private)

### irishrail
An open-source educational reconstruction of Ireland's National Train Control Centre traffic-management system. Ingests live train data, renders both geographic and schematic (Beck-style) maps, and includes a block-occupation conflict model, a mock interlocking/signaller, and scenario-based training simulations with scoring.
`Python · FastAPI · SQLite/DuckDB · MapLibre/PixiJS · GTFS-Realtime`
**Status:** In development

### law_rag
A legal knowledge-graph and RAG chatbot for Irish law. Scrapes and parses Acts, Statutory Instruments, and court judgments, embeds them, stores relationships in a graph database, and answers questions with cited sources, follow-up suggestions, and interactive graph visualisations.
`Next.js · Node.js · PostgreSQL + FalkorDB · embeddings/RAG · graph viz`
**Status:** In development

### family-tree (Craobh)
A searchable family tree of Ireland built from public historical records — the 1901 and 1911 censuses, civil registration, and wills. Links people across record sets via statistical record linkage (millions of person mentions) and renders a geocoded, hex-binned national map.
`Next.js · Drizzle/PostgreSQL · Python · splink · DuckDB`
**Status:** In development

### PWA Apps
A monorepo of white-label Progressive Web App concepts for small businesses — QR ordering, virtual queues, booking, loyalty — delivered as branded, installable web apps on a subscription model.
`pnpm monorepo · Next.js · Astro · Supabase`
**Status:** In development

### Letterbooked
A book discovery and review platform inspired by Letterboxd, with a Django REST API, JWT authentication, and a React SPA — book/author management, ratings, reviews, and a reading diary.
`Django REST Framework · React · PostgreSQL`
**Status:** Open source · [GitHub](https://github.com/williamomeara/letterbooked)

### Headlock
A full-stack SaaS platform that kept AI agents in continuous session loops to maximise the value of per-request AI subscriptions — web dashboard (PWA), CLI, real-time WebSocket status, JWT auth with email verification, tiered billing, and monitoring.
`FastAPI · React · PostgreSQL/Redis · WebSockets · Docker`
**Status:** Archived — the provider's per-request pricing model has since changed, retiring its core use case.

## Mobile Apps

### Éist
A Flutter audiobook app that turns EPUB and PDF files into natural-sounding audio using on-device AI text-to-speech — fully offline, no subscription. Engineered an OGG Opus pipeline that cut audio file sizes by ~93%.
`Flutter · on-device AI TTS (ONNX) · just_audio · SQLite`
**Status:** Live · 2,000+ downloads · [Website](https://eist.app) · [App Store](https://apps.apple.com/ie/app/eist-audiobook-reader/id6759532747) · [Google Play](https://play.google.com/store/apps/details?id=io.eist.app)

### Theory Test Free
A free Irish driver theory-test app spanning a Flutter mobile client, a web admin dashboard, a landing site, and a Supabase backend with a full content authoring and publishing pipeline.
`Flutter · Next.js · Astro · Supabase · pnpm monorepo`
**Status:** In development

### Are We There Yet
A location-aware alarm app that wakes you as you approach your stop on a train, bus, or coach — GPS-triggered, silent-mode compatible, with a clean layered architecture and golden/integration test coverage.
`Flutter · Riverpod · Drift (encrypted) · geolocator/flutter_map`
**Status:** In development

### Naptime Over
An Android app that schedules smarter naps and wake-ups from ambient sensor data, with a rule builder (audio, location, time, motion), background scheduling, and in-app billing.
`Kotlin · Jetpack Compose · Hilt · Room · WorkManager`
**Status:** In development

### Touchpad
Turns your smartphone into a wireless multi-touch trackpad for your computer — scroll, pinch, rotate, and swipe over local WiFi with zero-config mDNS pairing, cross-platform across desktop and mobile.
`Flutter (Melos monorepo) · mDNS · native gesture/input APIs`
**Status:** In development

## Machine Learning

### Maximum Clique Enumeration using Machine Learning
A supervised-learning framework for the NP-hard problem of maximum clique enumeration. Developed an edge-based approach with feature engineering to predict edges not part of any maximum clique, enabling graph pruning that outperforms node-based methods and scales to larger instances. (Final-year project, UCD.)
`Python · machine learning · graph algorithms`
**Status:** Academic · [Download FYP PDF](/files/maximum-clique-fyp.pdf)
