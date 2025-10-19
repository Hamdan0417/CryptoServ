<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crypto Serv - Technical README</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Source+Code+Pro&family=Tajawal:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Tajawal', sans-serif;
            background-color: #0D1117;
            color: #C9D1D9;
        }
        h1, h2, h3, h4 {
            color: #FFFFFF;
            font-weight: 700;
            border-bottom: 1px solid #30363D;
            padding-bottom: 0.5rem;
            margin-bottom: 1rem;
        }
        h1 { font-size: 2.5rem; }
        h2 { font-size: 2rem; margin-top: 2.5rem; }
        h3 { font-size: 1.5rem; margin-top: 2rem; border-bottom: none;}
        p, li {
            color: #C9D1D9;
            line-height: 1.7;
        }
        a {
            color: #58A6FF;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
        ul {
            list-style-type: disc;
            padding-right: 2rem; /* Adjusted for RTL if needed, but keeping LTR for code doc */
            padding-left: 2rem;
        }
        li {
            margin-bottom: 0.5rem;
        }
        code.inline-code {
            background-color: rgba(110, 118, 129, 0.4);
            padding: 0.2em 0.4em;
            margin: 0;
            font-size: 85%;
            border-radius: 6px;
            font-family: 'Source Code Pro', monospace;
        }
        pre {
            background-color: #161B22;
            padding: 1rem;
            border-radius: 8px;
            border: 1px solid #30363D;
            overflow-x: auto;
            margin-top: 1rem;
            margin-bottom: 1rem;
        }
        code {
            font-family: 'Source Code Pro', monospace;
            color: #C9D1D9;
        }
    </style>
</head>
<body class="antialiased">

    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-12">
        <h1 class="text-4xl font-extrabold mb-4">Crypto Serv: The All-in-One Crypto Services Ecosystem</h1>
        <p class="text-xl text-gray-400 mb-8">Technical README</p>

        <!-- Section 1: Project Overview -->
        <section>
            <h2>1. Project Overview</h2>
            <p>
                <strong>Crypto Serv</strong> is not just a cryptocurrency; it is a comprehensive, service-oriented ecosystem designed to address critical gaps in the blockchain and digital asset industry. Our mission is to build a trusted, centralized hub that connects talent, projects, investors, and service providers.
            </p>
            <p>
                This document outlines the full technical and functional requirements for building the Crypto Serv web platform. It is intended for the development team and provides a detailed roadmap for implementation.
            </p>
            <p>
                <strong>Live Prototype:</strong> A live, interactive prototype of the landing page can be viewed <a href="https://example.com/prototype-link" target="_blank">here</a>. <em>Note: This is a placeholder link.</em>
            </p>
        </section>

        <!-- Section 2: Core Platform Features -->
        <section>
            <h2>2. Core Platform Features (Functional Requirements)</h2>
            <p>The platform will be a multi-faceted web application with several key modules.</p>

            <h3>2.1. User Authentication & Wallet Management</h3>
            <ul>
                <li><strong>Primary Authentication:</strong> Users must be able to connect their Web3 wallet (e.g., MetaMask, Trust Wallet) as the primary method of identification and login.</li>
                <li><strong>Profile Creation:</strong> After connecting a wallet, users can create a profile.
                    <ul>
                        <li><strong>User Types:</strong> The system must support distinct profile types: "Talent" (Job Seeker), "Employer" (Company/Individual), and "Investor".</li>
                        <li><strong>Profile Data:</strong> Basic information (username, email), social links, and specific data relevant to their user type (e.g., CV for Talent, company details for Employers).</li>
                    </ul>
                </li>
                <li><strong>Dashboard:</strong> Each user will have a personalized dashboard to manage their activities on the platform.</li>
            </ul>

            <h3>2.2. The Job Portal</h3>
            <ul>
                <li><strong>For Employers:</strong>
                    <ul>
                        <li><strong>Company Profile:</strong> Create and manage a detailed company profile.</li>
                        <li><strong>Post a Job:</strong> An intuitive form to post job openings with fields for title, description, location (including "Remote"), contract type, required skills, and salary range.</li>
                        <li><strong>Applicant Tracking:</strong> A dashboard to view, filter, and manage applications.</li>
                        <li><strong>Tiered Access:</strong> Employers may need to hold a certain amount of <code class="inline-code">SERV</code> tokens to unlock premium features.</li>
                    </ul>
                </li>
                <li><strong>For Talent (Job Seekers):</strong>
                    <ul>
                        <li><strong>Professional Profile:</strong> Create a detailed profile, upload a CV (PDF).</li>
                        <li><strong>Job Search & Filtering:</strong> Advanced search functionality.</li>
                        <li><strong>One-Click Apply:</strong> A simple application process.</li>
                        <li><strong>Application Status:</strong> Track the status of job applications.</li>
                    </ul>
                </li>
            </ul>

            <h3>2.3. Services Marketplace</h3>
            <ul>
                <li><strong>Project Quality Certification:</strong> A submission form, an admin review interface, and a public registry of certified projects.</li>
                <li><strong>Licensing Assistance:</strong> An informational page with a contact form.</li>
                <li><strong>Support for Distressed Projects:</strong> An application form and a secure backend portal for evaluation.</li>
                <li><strong>Investor Network Portal:</strong> An exclusive, token-gated portal for verified investors to view vetted opportunities.</li>
            </ul>

            <h3>2.4. `SERV` Token Integration & Airdrop Portal</h3>
            <ul>
                <li><strong>Payment System:</strong> Use <code class="inline-code">SERV</code> for platform services with a discount mechanism.</li>
                <li><strong>Staking & Loyalty Dashboard:</strong> A user dashboard to stake tokens, view rewards, and claim airdrops.</li>
            </ul>

            <h3>2.5. Admin Panel</h3>
            <ul>
                <li>A comprehensive and secure admin dashboard for user, job, and service management, airdrop configuration, and platform analytics.</li>
            </ul>
        </section>

        <!-- Section 3: Recommended Technical Stack -->
        <section>
            <h2>3. Recommended Technical Stack</h2>
            <ul>
                <li><strong>Frontend:</strong> <strong>Next.js</strong> (React Framework) with <strong>Tailwind CSS</strong>.</li>
                <li><strong>Backend:</strong> <strong>Node.js</strong> with <strong>Express.js</strong> (or NestJS).</li>
                <li><strong>Database:</strong> <strong>PostgreSQL</strong>.</li>
                <li><strong>Blockchain Interaction (Frontend):</strong> <strong>Ethers.js</strong> or <strong>Web3.js</strong>.</li>
                <li><strong>Smart Contract Language:</strong> <strong>Solidity</strong>.</li>
                <li><strong>Smart Contract Development Environment:</strong> <strong>Hardhat</strong>.</li>
                <li><strong>Deployment:</strong> <strong>Vercel</strong> (Frontend), and a cloud provider like <strong>AWS</strong>, <strong>Google Cloud</strong>, or <strong>Heroku</strong> (Backend).</li>
            </ul>
        </section>

        <!-- Section 4: Key Technical & Architectural Requirements -->
        <section>
            <h2>4. Key Technical & Architectural Requirements</h2>
            <h3>4.1. Smart Contracts</h3>
            <ul>
                <li><strong><code class="inline-code">SERV</code> Token:</strong> Must be a BEP-20 or ERC-20 compliant token following OpenZeppelin standards.</li>
                <li><strong>Staking Contract:</strong> A separate contract for staking logic and reward calculation.</li>
                <li><strong>Security:</strong> A professional, third-party security audit is non-negotiable before mainnet deployment.</li>
            </ul>
            <h3>4.2. Backend & API</h3>
            <ul>
                <li>Must be built as a <strong>RESTful API</strong>.</li>
                <li>All endpoints must be authenticated and authorized based on user roles.</li>
            </ul>
            <h3>4.3. Database Schema (High-Level)</h3>
            <ul>
                <li><code class="inline-code">Users</code> (wallet_address, username, email, profile_type, etc.)</li>
                <li><code class="inline-code">Profiles</code> (linked to Users, contains detailed info like bio, experience, etc.)</li>
                <li><code class="inline-code">Companies</code> (linked to employer Users)</li>
                <li><code class="inline-code">Jobs</code> (linked to Companies, contains all job details)</li>
                <li><code class="inline-code">JobApplications</code> (links a User profile to a Job)</li>
                <li><code class="inline-code">Services</code> (e.g., <code class="inline-code">Certifications</code>, <code class="inline-code">SupportRequests</code>)</li>
                <li><code class="inline-code">Stakes</code> (user_address, amount, timestamp)</li>
            </ul>
            <h3>4.4. General Requirements</h3>
            <ul>
                <li><strong>Responsive Design:</strong> Fully optimized for mobile, tablet, and desktop.</li>
                <li><strong>Performance:</strong> Fast and optimized for quick load times.</li>
                <li><strong>Security:</strong> Standard web security practices must be implemented.</li>
            </ul>
        </section>
        
        <!-- Section 5: Getting Started -->
        <section>
            <h2>5. Getting Started (For Developers)</h2>
            <p>1. <strong>Clone the repository:</strong></p>
            <pre><code>git clone https://github.com/Crypto-Serv/platform.git
cd platform</code></pre>

            <p>2. <strong>Install Dependencies:</strong></p>
            <pre><code># From the root
npm install

# Install client dependencies
cd client
npm install

# Install server dependencies
cd ../server
npm install</code></pre>

            <p>3. <strong>Environment Variables:</strong></p>
            <p>Create a <code class="inline-code">.env.local</code> file in both the <code class="inline-code">/client</code> and <code class="inline-code">/server</code> directories. Populate them with the necessary variables (Database URL, JWT Secret, RPC Node URL, etc.). Refer to <code class="inline-code">.env.example</code>.</p>

            <p>4. <strong>Run the Development Servers:</strong></p>
            <pre><code># Run the backend server (from /server)
npm run dev

# Run the frontend server (from /client)
npm run dev</code></pre>
        </section>

    </main>

</body>
</html>
