# CyberLab — Student Vulnerability Practice Platform

A web platform that lets students log in and spin up vulnerable machines from a local server. Each user gets their own isolated environment — deploy it, hack it, delete it when done.

## What it does

Students log in, pick a vulnerable machine from the available list, and deploy it. Every environment is isolated per user so nobody interferes with anyone else's session. When you're done, delete it and it's gone.

Think mini HackTheBox, but self-hosted and built from scratch.

## Why I built it

School project. I wanted to build something that actually solves a real problem — students need safe, isolated environments to practice cybersecurity without setting up their own VMs every time.

## How it works

- **Next.js** frontend — login, dashboard, machine selection, deploy/delete controls
- **Firebase** handles user authentication and credentials — each login gets a unique user ID
- **Isolation** is based on that user ID — your environment is yours, nobody else can touch it
- **Local server** hosts and deploys the vulnerable machines
- Currently supports 3 machines from VulnHub

## Stack

- Frontend: Next.js
- Backend/Auth: Firebase
- Deployment: Local web server
- Machines: VulnHub (3 available)

## Features

- Student login and authentication
- Deploy a vulnerable machine with one click
- Full environment isolation per user ID
- Delete environment when done
- Local server deployment — no cloud costs

## Setup

```bash
# Install dependencies
npm install

# Add your Firebase config to .env.local
NEXT_PUBLIC_FIREBASE_API_KEY=your_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_domain

# Run locally
npm run dev
```

## What I learned

Isolation doesn't have to be complicated — tying environments to unique IDs keeps things clean without needing heavy infrastructure. Firebase made auth fast to implement so I could focus on the actual platform logic.

---

> Built to give students a place to practice without the setup headache.