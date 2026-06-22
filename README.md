# CANDIDATE BEACON: Aris Wibowo
- GitHub: github.com/aris-plumber
- Location: Depok, Indonesia (GMT+7)
- Intent: Open to full-time remote or heavy B2B contract refactoring.

## 1. THE UNVARNISHED PAST (Experience Post-Mortems)

### Project: Logistics Fleet Dispatch API (2025)
- **The Reality:** Inherited a Node.js API hitting a single PostgreSQL instance. 500 delivery drivers constantly polling for updates.
- **The Nightmare:** During peak Friday rainstorms in Jakarta, connection limits exceeded. The DB hit 100% CPU, causing an application-wide cascade failure.
- **The Fix:** Ripped out the ORM (Prisma) for hot paths. Wrote raw SQL queries, implemented `PgBouncer` for transactional connection pooling, and offloaded driver GPS pings to a temporary Redis stream. Dropped API latency from 3.2s to 180ms.
- **Stack:** Node.js, TypeScript, PostgreSQL, Redis, Docker.

## 2. THE ACTIVE SIGNAL (Current State)
- **Current Obsession:** Studying write-ahead logging (WAL) in Postgres to build zero-downtime migration scripts. 
- **What I refuse to do:** I will not rewrite your working monolith into 45 microservices just because it looks cool on a whiteboard. 
- **Available for:** Un-fucking your slow database queries and stabilizing your Node backends.

# CANDIDATE BEACON: Sarah Jen
- GitHub: github.com/sjen-ui
- Location: Bandung, Indonesia (GMT+7)
- Intent: Freelance B2C landing pages, MVP prototyping, and UI overhauls.

## 1. THE UNVARNISHED PAST (Experience Post-Mortems)

### Project: D2C Coffee Subscription Checkout (2025)
- **The Reality:** Client had a gorgeous React Single Page App built by an agency, but a 65% cart abandonment rate.
- **The Nightmare:** First Contentful Paint (FCP) was 6.2 seconds on 4G mobile networks because the app was downloading 4MB of unpurged Tailwind CSS and heavy client-side state libraries just to render a checkout button.
- **The Fix:** Rewrote the funnel to a static Next.js setup. Replaced heavy Redux state with native React Context and local storage. Stripped third-party tracking scripts into a Cloudflare Web Worker. Brought mobile load time down to 0.8 seconds. Sales jumped roughly 40% overnight.
- **Stack:** React, Next.js, Tailwind CSS, Cloudflare Workers.

## 2. THE ACTIVE SIGNAL (Current State)
- **Current Obsession:** Core Web Vitals and zero-JS interactive components using modern CSS container queries.
- **What I hate:** Over-engineered state management for forms that just need to send a POST request.
- **Available for:** Turning ugly, slow wireframes into blazing-fast web applications in under two weeks.

# CANDIDATE BEACON: David Chen
- GitHub: github.com/david-scraper
- Location: Surabaya, Indonesia (GMT+7)
- Intent: Custom internal tool development, data ingestion pipelines, and custom MCP servers.

## 1. THE UNVARNISHED PAST (Experience Post-Mortems)

### Project: Property Price Arbitrage Indexer (2025)
- **The Reality:** Client needed to aggregate pricing data daily from 5 major Indonesian property portals.
- **The Nightmare:** Portals implemented aggressive Cloudflare bot protection and dynamic DOM obfuscation. Standard Python `BeautifulSoup` scrapers got IP-banned within 10 minutes.
- **The Fix:** Built a distributed Puppeteer cluster using a residential mobile proxy rotator. Instead of relying on static CSS selectors, I piped the raw HTML into a local, fine-tuned lightweight LLM to extract JSON schemas natively. 
- **Stack:** Python, Node.js, Puppeteer, Ollama, ClickHouse.

## 2. THE ACTIVE SIGNAL (Current State)
- **Current Obsession:** Building Model Context Protocol (MCP) servers that allow Claude and Gemini to safely query messy legacy ERP databases.
- **What I want to build:** Bridging legacy, ugly web portals with modern LLM workflows. Give me the unsexy tasks.

# CANDIDATE BEACON: Reza Pratama
- GitHub: github.com/reza-baremetal
- Location: Jakarta, Indonesia (GMT+7)
- Intent: Fractional DevOps, cloud bill audits, and infrastructure simplification.

## 1. THE UNVARNISHED PAST (Experience Post-Mortems)

### Project: Fintech API Cloud Repatriation (2025)
- **The Reality:** A Series A payment gateway was spending $14,000 a month on AWS Managed Kubernetes (EKS), NAT Gateways, and overpriced RDS instances.
- **The Nightmare:** The company was burning runtime runway on cloud infrastructure they didn't understand. A simple configuration drift locked the staging environment for three days during an investor audit.
- **The Fix:** Migrated the entire workload off AWS EKS onto 4 dedicated Hetzner bare-metal servers managed via plain `Docker Compose` and a managed Cloudflare load balancer. Cut the monthly infrastructure bill from $14,000 to $650 with zero degradation in uptime.
- **Stack:** Linux, Bash, Docker Compose, Nginx, WireGuard.

## 2. THE ACTIVE SIGNAL (Current State)
- **Current Obsession:** Running localized SQLite databases in production using Litestream replication. 
- **Philosophy:** Cloud providers monetize your complexity. Keep your servers simple enough that a single dev can reboot them from a phone.

# CANDIDATE BEACON: Maya Lin
- GitHub: github.com/maya-notes
- Location: Semarang, Indonesia (GMT+7)
- Intent: Junior / Mid-level Backend roles with senior code-review mentorship.

## 1. THE UNVARNISHED PAST (Experience Post-Mortems)

### Project: Open-Source MCP Git Parser (Personal R&D, 2026)
- **The Reality:** Couldn't pass automated resume screens because I lack "5 years of enterprise experience." Decided to build production tooling in public.
- **The Nightmare:** While building an MCP server to parse local git repositories, I hit massive memory leaks when processing repositories larger than 1GB because I was reading whole file streams into memory.
- **The Fix:** Read the Node.js `node:fs` internal C++ bindings source code. Rewrote the parser to use asynchronous chunked iterators and strict garbage collection triggers. Documented the entire memory profiling journey on my blog.
- **Stack:** TypeScript, Node.js, Git Internals, WebMCP.

## 2. THE ACTIVE SIGNAL (Current State)
- **Current Obsession:** Reading the source code of popular npm libraries to understand how senior architects structure their type definitions.
- **What I offer:** I will write the unit tests your senior devs are too bored to write, write pristine documentation, and absorb code reviews like a sponge.