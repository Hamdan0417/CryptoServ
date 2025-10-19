# Crypto Serv: The All-in-One Crypto Services Ecosystem

## Table of Contents
- [Project Overview](#project-overview)
  - [Mission](#mission)
  - [Live Prototype](#live-prototype)
- [Core Platform Features](#core-platform-features)
  - [User Authentication & Wallet Management](#user-authentication--wallet-management)
  - [Job Portal](#job-portal)
  - [Services Marketplace](#services-marketplace)
  - [SERV Token Integration & Airdrop Portal](#serv-token-integration--airdrop-portal)
  - [Admin Panel](#admin-panel)
- [Recommended Technical Stack](#recommended-technical-stack)
- [Key Technical & Architectural Requirements](#key-technical--architectural-requirements)
  - [Smart Contracts](#smart-contracts)
  - [Backend & API](#backend--api)
  - [High-Level Database Schema](#high-level-database-schema)
  - [General Platform Requirements](#general-platform-requirements)
- [Getting Started](#getting-started)
  - [Repository Setup](#repository-setup)
  - [Environment Variables](#environment-variables)
  - [Running the Development Servers](#running-the-development-servers)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview
Crypto Serv is a comprehensive, service-oriented ecosystem that goes beyond a traditional cryptocurrency. The platform addresses critical gaps in the blockchain and digital asset industry by providing a trusted, centralized hub where talent, projects, investors, and service providers can collaborate.

This README serves as the master technical reference for the development team, outlining the functional scope, architectural expectations, and onboarding steps required to build and maintain the Crypto Serv web platform.

### Mission
- Connect Web3 talent with meaningful career opportunities.
- Offer reliable services for project certification, licensing support, and distressed project recovery.
- Provide investors with access to curated, vetted opportunities in a secure environment.
- Create tangible utility for the SERV token through staking, payments, and loyalty incentives.

### Live Prototype
A live, interactive prototype of the landing page will be provided as the design stabilizes. (Note: The link is currently a placeholder.)

---

## Core Platform Features
Crypto Serv is designed as a multi-faceted web application with the following primary modules:

### User Authentication & Wallet Management
- **Primary Authentication:** Users authenticate by connecting a Web3 wallet (e.g., MetaMask, Trust Wallet).
- **Profile Creation:** Wallet login is followed by guided profile setup.
- **User Types:** Distinct personas are supported: **Talent (Job Seeker)**, **Employer (Company/Individual)**, and **Investor**.
- **Profile Data:** Capture usernames, optional email addresses, social links, and persona-specific details (e.g., résumé/CV for Talent, company information for Employers).
- **Dashboard:** Each persona receives a tailored dashboard summarizing their activity across the platform.

### Job Portal
**For Employers**
- Maintain a rich company profile with branding assets and contact information.
- Post job openings with fields for title, description, location (including remote), contract type, required skills, and salary range.
- Track applicants through a dedicated dashboard with filtering, status updates, and messaging.
- Unlock premium hiring tools by meeting SERV token holding thresholds.

**For Talent**
- Build a professional profile with work history, skills, and an uploaded CV (PDF).
- Discover opportunities through advanced search and filtering controls.
- Submit one-click applications using the connected profile and track their status in real time.

### Services Marketplace
- **Project Quality Certification:** Intake form for submissions, an administrative review workflow, and a public registry of certified projects.
- **Licensing Assistance:** Informational landing page coupled with a contact form for engagement requests.
- **Support for Distressed Projects:** Secure application form routed to an internal evaluation portal.
- **Investor Network Portal:** Token-gated area where verified investors access vetted deal flow and supporting documentation.

### SERV Token Integration & Airdrop Portal
- **Payments:** Support platform transactions using SERV with optional discounts to incentivize usage.
- **Staking & Loyalty Dashboard:** Enable users to stake tokens, monitor accrued rewards, and claim airdrops.
- **Airdrop Configuration:** Allow administrators to create, schedule, and manage airdrop campaigns.

### Admin Panel
Provide a secure, role-based control center for:
- Managing users, profiles, and company records.
- Reviewing and moderating job postings and service requests.
- Configuring staking pools, airdrop events, and SERV-based incentives.
- Monitoring platform analytics, transaction health, and security alerts.

---

## Recommended Technical Stack
| Layer | Technology |
| --- | --- |
| Frontend | Next.js (React) with Tailwind CSS |
| Backend | Node.js with Express.js or NestJS |
| Database | PostgreSQL |
| Blockchain Interaction (Frontend) | Ethers.js or Web3.js |
| Smart Contract Language | Solidity |
| Smart Contract Tooling | Hardhat |
| Deployment | Vercel (frontend) and AWS, Google Cloud, or Heroku (backend) |

---

## Key Technical & Architectural Requirements

### Smart Contracts
- SERV token must follow BEP-20 or ERC-20 standards using OpenZeppelin implementations.
- Deploy dedicated staking contracts responsible for reward calculation and distribution.
- Commission third-party security audits before mainnet release.

### Backend & API
- Expose functionality through a RESTful API.
- Enforce authentication and role-based authorization on all endpoints.
- Log key actions for observability, compliance, and security monitoring.

### High-Level Database Schema
| Table | Purpose |
| --- | --- |
| **Users** | Stores wallet address, username, optional email, and persona type. |
| **Profiles** | Detailed persona information such as bio, experience, and links. |
| **Companies** | Employer-specific data linked to user accounts. |
| **Jobs** | Job postings with metadata (skills, salary range, etc.). |
| **JobApplications** | Mapping between talent profiles and jobs with status tracking. |
| **Services** | Records for certification requests, licensing support, and project recovery submissions. |
| **Stakes** | Token stakes, including wallet address, amount, and timestamps. |

### General Platform Requirements
- Deliver a fully responsive experience across mobile, tablet, and desktop breakpoints.
- Optimize for fast load times and low-latency data access.
- Apply best-practice web security measures (input validation, rate limiting, CSRF/XSS protections, secure headers).

---

## Getting Started

### Repository Setup
```bash
# Clone the repository
git clone https://github.com/Crypto-Serv/platform.git
cd platform

# Install root-level dependencies
npm install

# Install frontend dependencies
cd client
npm install

# Install backend dependencies
cd ../server
npm install
```

### Environment Variables
Create a `.env.local` file in both the `/client` and `/server` directories and populate the required configuration values (e.g., database URL, JWT secret, RPC node URL). Consult any provided `.env.example` files for reference.

### Running the Development Servers
```bash
# From /server
npm run dev

# In a separate terminal from /client
npm run dev
```

---

## Contributing
Pull requests are welcome! Please open an issue first to discuss major changes. Ensure code is linted, tested, and adheres to the architectural guidelines outlined above before submission.

## License
The licensing terms for Crypto Serv will be defined as the project approaches launch. Until then, all rights are reserved.
