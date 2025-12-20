# duh.zo
## Building the Zo OS
### The 111 Elite Hacker Collective

**Version 1.0 | December 2024**

---

## Vision

**duh.zo** is a global network of elite hackers building the Zo OS - the infrastructure layer for physical communities in the digital age. We are creating an open source ecosystem of tools that power networked living spaces, from operations automation to reputation systems to community coordination.

From the original Zo House documentation: *"We're building the Operating System for Becoming: Hospitality 2.0, IoT Dashboard, Questing Map, and Community Tokens."* Now we're opening this OS to the world.

**Our Thesis:** The future of human coordination happens at the intersection of physical spaces and digital protocols. We're building the OS that makes this possible.

---

## The 111 Elite Hackers

**duh.zo** is not just another open source project. It's a **selective builder collective** based on a single competitive leaderboard:

- **∞ Open Contributors** - Anyone can contribute (unlimited)
- **The 111 Elite Hackers** - Top 111 ranked contributors on the global leaderboard
  - **The 11 Elite Vibe Keepers** - Rank #1-#11 (must have 11+ code contributions to qualify for this status)
  - **The 100 Leaderboard Hackers** - Rank #12-#111

**How The Leaderboard Works:**

Everyone who contributes gets ranked on a single global performance leaderboard:
- **Ranking Factors:** Recent contribution velocity (last 3 months), code quality, architectural impact, PR reviews, community help
- **Updates:** Rankings refresh weekly based on activity
- **Competitive:** Your rank can go up or down based on what you ship

**The 11 Elite Vibe Keepers (Ranks #1-#11):**
- **Requirements:** 
  1. Rank in top 11 positions on the leaderboard
  2. Have at least 11 meaningful code contributions
- **Qualifier Gate:** If you rank #1-#11 but only have 9 code contributions, you don't get elite vibe keeper status yet - keep shipping code PRs!
- **Highly Competitive:** Top 11 positions change weekly - you must maintain performance
- **Stop Contributing:** Drop in rankings → lose top 11 status
- **Elite Privileges:** 
  - Weekly Thursday 9 PM IST strategy calls (inner circle)
  - Maximum $Zo reward tier
  - Direct architectural input and can propose new initiatives
  - Priority Zo House booking
  - Special "Elite Vibe Keeper" recognition

**The 100 Leaderboard Hackers (Ranks #12-#111):**
- **Requirement:** Rank in positions 12-111 on the global leaderboard
- **No minimum contributions:** Just need to rank in top 111
- **Dynamic Competition:** Active fight for these 100 spots
- **Path Upward:** Keep shipping quality code to break into top 11, AND accumulate 11+ code contributions

**What Counts as "Code Contribution"?**
- Features, architecture work, complex bug fixes
- NOT documentation, typos, or trivial changes  
- Maintainers validate what counts as "code"
- Quality matters - one excellent PR > ten trivial ones

**The Ranking Tiers:**
- **#1-#11:** Elite Vibe Keepers (if they have 11+ code contributions)
- **#12-#50:** High-tier leaderboard hackers
- **#51-#111:** Entry-tier leaderboard hackers
- **#112+:** Open contributors grinding to break into top 111

**Benefits Scale by Rank:**
- **Top 11:** Highest $Zo multiplier, weekly calls, architectural authority
- **Top 50:** High $Zo multiplier, priority Zo House access
- **Top 111:** Above-baseline $Zo, access to 111-only Telegram, voting rights

**It's Pure Competition:** One global leaderboard. Top 111 are the elite. Top 11 (with 11+ code contributions) are the vibe keepers.

---

## What We're Building

An interconnected suite of open source tools that form the Zo OS - a complete operating system for running networked physical communities. These projects are **already partially built and in use** at Zo Houses across multiple cities. We're now opening them to the world for contributors to help us scale and improve them.

### The 6 Core Projects

These are **independent microservices** that together form the Zo OS:

**Project 1: Zo Web Platform** (`zo.xyz`)

**GitHub:** https://github.com/ZoHouse/zo.xyz  
**Architecture:** Nx 17.1.3 monorepo with multiple Next.js 14 applications

**Applications (9 apps running on different ports):**
- **admin** (4201) - Central Admin System (CAS) for back-office management
- **website** (4202) - Public-facing Zo World website (main landing)
- **dashboard** (4203) - Member dashboard and Zo Passport interface
- **pms** (4204) - Property Management System
- **payment** (4205) - Payment processing portal
- **web-checkin** (4206) - Guest self-service check-in
- **meme** (4208) - Meme generator tool
- **comic** (4209) - Comic reader
- **zo-ops** (4210) - Operations dashboard

**Backend:**
- **ops-backend** (4211) - Express.js API server

**Tech Stack:**
- Framework: Next.js 14, React 18
- Build System: Nx 17.1.3 monorepo
- Language: TypeScript
- UI: Tailwind CSS, Ant Design, MUI, shadcn/ui
- State: React Query v3/v5
- Web3: wagmi, viem, RainbowKit
- Maps: Mapbox GL, Leaflet
- Backend: Express.js, PostgreSQL, Redis
- **Deployment: AWS ECS (Docker containers)**
- CI/CD: GitHub Actions with automated task definitions

**Docker:**
- Separate Dockerfiles for Next.js apps and Node.js backend
- Task definitions managed via scripts/generate-task-definition.sh
- Secrets fetched from AWS via scripts/fetch-secrets.sh
- Changed apps auto-detected via scripts/detect-changed-apps.sh

**Shared Libraries:**
- `@zo/auth` - Authentication & API hooks (130+ API endpoints)
- `@zo/moal` - Common UI components
- `@zo/zud` - Form components & CRUD interfaces
- `@zo/assets/*` - Icons (130+), brands, lotties
- `@zo/coal/*` - Base UI & typography
- `@zo/utils/*` - String, number, auth, web3, hooks utilities
- `@zo/definitions/*` - TypeScript type definitions

**Status:** Production monorepo powering 9+ applications. Complex Nx workspace with extensive shared library ecosystem. The **website** app (port 4202) is the main zo.xyz landing page.

---

**Project 2: Zo World Questing Map** (`zohm`)

**GitHub:** https://github.com/ZoHouse/zohm  
"A Life Design Simulation Engine" - The gamified reality design layer

**Features:**
- **Vibe Score** - Real-time alignment metric (0-100%)
- **Quest System** - Structured quests with token rewards (Social, Creative, Physical, Digital)
- **Interactive Node Map** - 3D Mapbox visualization of global Zo Nodes
- **Zo Passport** - Digital identity with Citizen → Founder progression
- **Culture System** - Declare cultures, matching, community formation
- **Quantum Sync** - Voice quest with AssemblyAI integration
- **Zo Houses & Nodes** - Physical infrastructure as cultural routers

**Tech Stack:**
- Next.js 15, React 19, TypeScript 5
- Supabase (PostgreSQL with realtime subscriptions)
- Mapbox GL JS (3D visualization)
- AssemblyAI (voice), OpenAI (narrative)
- Base L2 & Avalanche Fuji (blockchain)

**The Reality Engine Loop:**
```
Observe → Model → Simulate → Reinforce
(Captures behavior → Computes vibe → Generates quests → Rewards progress)
```

**Status:** Production app with complete quest system, vibe score algorithm, and node visualization. This is the **core gamification layer** of the Zo ecosystem.

---

**Project 3: Hospitality 2.0 Bot** (`Hospitality-2.0`)

**GitHub:** https://github.com/ZoHouse/Hospitality-2.0  
**Agentic automation microservice** for housekeeping operations:

**What it does:**
- Multi-persona LangGraph workflows (housekeeping staff + captain personas)
- Intelligent task assignment across 18+ property zones
- WhatsApp integration for real-time staff communication
- PMS integration (automated check-in/check-out reports via Playwright)
- Time tracking and performance analytics
- Natural language special request creation

**Tech Stack:**
- Backend: Python 3.11+, FastAPI
- AI/Agents: LangGraph for multi-persona workflows (OpenAI + Groq)
- Database: PostgreSQL (Supabase) - separate instance from web platform
- Automation: Playwright for PMS scraping
- Messaging: WhatsApp (Whapi.Cloud for groups + Facebook Cloud API for individuals)
- Deployment: [TO BE FILLED]

**Key Features:**
- 18+ predefined property zones with task lists
- 4 housekeeping staff + 1 captain with shift schedules
- Intent detection from natural language keywords
- Automated daily reports at 9 AM via WhatsApp
- Role-based persona routing
- Time tracking with efficiency metrics

**Status:** Production-ready, running in Zo Houses. This is a **separate Python service** that the web platform can call via REST API.

**Key Areas for Contribution:**
- New LangGraph personas (maintenance, security, etc.)
- Additional PMS integrations
- Advanced analytics and reporting
- Voice integration (WhatsApp voice messages)
- Multi-language support
- Better intent detection algorithms

**Integration Points:**
- REST API that web platform (`/pm/hospitality2.0`) can call
- Shares authentication with Zo API
- Could integrate with Passport SDK for staff reputation

---

**Project 5: Zo Passport SDK** (`zopassport`)

**GitHub:** https://github.com/ZoHouse/zopassport  
**npm:** https://www.npmjs.com/package/zopassport  
**Already published on npm as `zopassport`** - "One line reputation to rule the world"

A portable reputation and identity system that any application can integrate. Complete authentication, onboarding, and passport experience.

**Installation:**
```bash
npm install zopassport
# or
npx create-zopassport  # Creates full demo app
```

**Current Features:**
- **Authentication**: Phone + OTP flow with automatic token refresh
- **Avatar Generation**: AI-powered avatars (Bro/Bae body types with polling status)
- **Passport Card**: Leather texture design with Founder/Citizen variants, progress ring
- **Onboarding Flow**: Nickname input, location detection, avatar preview
- **Wallet Integration**: Built-in wallet for $Zo and Zo World assets
- **Universal Support**: Works on web (React) and mobile (React Native via react-native-web)

**React Components:**
```tsx
import { 
  ZoPassportProvider, 
  useZoPassport, 
  ZoLanding, 
  ZoOnboarding, 
  ZoPassportCard,
  WalletScreen 
} from 'zopassport/react';
```

**Core SDK:**
```typescript
import { ZoPassportSDK } from 'zopassport';

const sdk = new ZoPassportSDK({
  clientKey: 'your-client-key',
  autoRefresh: true,
  storageAdapter: new AsyncStorageAdapter(AsyncStorage) // For React Native
});

// Get reputation
await sdk.passport.getReputation(userId)

// Track contribution  
await sdk.passport.trackContribution({
  userId, type: 'github-pr', value: { repo, prNumber }
})

// Check access
await sdk.passport.checkAccess(userId, 'zo-house-bangalore')

// Wallet operations
await sdk.wallet.getBalance()
await sdk.wallet.getTransactions()
```

**Storage Adapters:**
- Web: localStorage (default)
- React Native: AsyncStorageAdapter
- Server/Testing: MemoryStorageAdapter

**Tech Stack:**
- TypeScript
- React (web) & React Native (mobile)
- react-native-web for universal components
- Vite / Next.js compatible
- CDN-hosted assets

**Status:** Production npm package. Core SDK shipped and in use. Ready for:
- Additional blockchain integrations (currently supports Solana)
- Python/Go/Ruby SDK wrappers
- Advanced reputation algorithms
- Cross-platform contribution tracking
- External community integrations

**Vision:** Universal reputation layer for physical communities. Any coliving space, hacker house, or DAO can integrate Zo Passport to track member contributions.

---

**Project 4: Zo World Mobile App** (`ZoWorldmobile`)

**GitHub:** https://github.com/ZoHouse/ZoWorldmobile  
Mobile-first community coordination app - "Where Vibes Become Reality":

**Features:**
- 🎮 Quantum Sync - Audio-based quest system with leaderboards & token rewards
- 🏠 IRL Bookings - Book stays, workspaces, and experiences at Zo properties
- 💬 Community - Real-time chat, bulletin boards, social features
- 🔗 Web3 Native - WalletConnect v2, multi-chain support, NFT gallery
- 📱 9 App Icons - Customizable app appearance
- 🎨 ZUI Design System - 100+ custom components

**Tech Stack:**
- Framework: React Native 0.73.6
- Language: TypeScript 5.0.4
- UI: Native Base 3.4.28, ZUI Design System (28 core components, 14 bottom sheets, 46 icons)
- Navigation: React Navigation 6.x
- State: TanStack Query (React Query) for data fetching
- Audio: react-native-audio-recorder-player (for Quantum Sync)
- Web3: Reown AppKit (WalletConnect v2), wagmi, viem
- Blockchain: Ethereum, Polygon, Arbitrum, Base
- Backend: Firebase (Analytics, Crashlytics, Messaging), Socket.io, Razorpay
- Animations: react-native-reanimated, Lottie

**Key Screens:**
- Home (Quantum Sync Dashboard)
- QuestAudio / QuestComplete
- Bulletin (Community Feed)
- IRL (Events & Bookings with full booking flow)
- AllChats (Messages with Socket.io)
- Profile with Passport integration
- AllWallets / AllZoNFTs

**Status:** Production-ready React Native app with 39 screens, extensive Web3 integration, and gamified quest system. Ready for iOS/Android deployment.

---

**Project 6: Zo Builder Bot** (`ZoBuilder-bot`)

**GitHub:** https://github.com/ZoHouse/ZoBuilder-bot  
Telegram bot that acts as the official community agent for Zo House builder network:

**Current Features:**
- **Commands**:
  - `/start` - Setup builder profile with phone OTP authentication
  - `/help` - List all available commands
  - `/profile` - View profile information and Builder Score
  - `/nominate @username` - Nominate a fellow builder for recognition
  - `/score` - Check your Builder Score
  - `/leaderboard` - View top builders in community
- **GitHub Integration**:
  - Real-time webhook integration with Zo House GitHub repos
  - Announces new commits, PRs, and issues in Telegram
  - Attributes GitHub activity to contributors
  - Tracks: commits, pull requests, issue creation/comments
- **Builder Score Calculation**:
  - GitHub activity (commits, PRs, issues)
  - Community nominations and engagement within Telegram
  - Telegram activity and participation
- **Automation**:
  - Automatic onboarding for new members
  - Weekly recap posts highlighting community achievements

**Tech Stack:**
- Python 3.8+ with python-telegram-bot framework
- GitHub webhooks via FastAPI/uvicorn webhook server
- MongoDB for data storage
- Telegram Bot API
- Phone OTP authentication via Zo API

**Database:**
- MongoDB collections for:
  - User profiles with GitHub usernames
  - Builder Scores and activity tracking
  - Nomination history
  - GitHub contribution events

**Deployment:**
- Bot server (bot.py) - Telegram bot handler
- Webhook server (webhooks.py) - GitHub webhook receiver
- Requires public URL endpoint for GitHub webhooks

**Status:** Core functionality built and running. Ready for:
- Multi-platform tracking (GitLab, Bitbucket)
- Advanced analytics and visualization
- $Zo token distribution integration
- Enhanced leaderboard features with wallet display
- Cross-house contributor tracking
- Integration with Passport SDK for unified reputation

---

### How They Work Together

**Microservices Architecture:**

```
                        ┌─────────────────┐
                        │   Zo API        │
                        │ (Phone OTP Auth)│
                        └────────┬────────┘
                                 │
            ┌────────────────────┼────────────────────┐
            │                    │                    │
            ▼                    ▼                    ▼
┌───────────────────┐  ┌──────────────────┐  ┌──────────────────┐
│  zo.xyz Monorepo  │  │  zohm (Questing) │  │ Hospitality Bot  │
│  (Next.js/Nx)     │  │  (Next.js 15)    │  │ (Python/FastAPI) │
│                   │  │                  │  │                  │
│ - 9 apps          │  │ - Vibe Score     │  │ - LangGraph      │
│ - website landing │  │ - Quest System   │  │ - WhatsApp       │
│ - admin, pms, etc │  │ - Node Map 3D    │  │ - PMS scraping   │
│ - @zo/auth        │  │ - Quantum Sync   │  │ - 18+ zones      │
└─────────┬─────────┘  └────────┬─────────┘  └─────────┬────────┘
          │                     │                       │
          │                     │                       │
          └─────────────────────┼───────────────────────┘
                                │
                                ▼
                   ┌────────────────────────┐
                   │   Zo Passport SDK      │
                   │   (npm: zopassport)    │
                   │                        │
                   │ - Reputation tracking  │
                   │ - Phone OTP auth       │
                   │ - Wallet integration   │
                   │ - Avatar generation    │
                   └───────────┬────────────┘
                               │
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
    ┌───────────────┐  ┌──────────────┐  ┌─────────────┐
    │ Builder Bot   │  │ Mobile App   │  │ External    │
    │ (Telegram)    │  │ (React       │  │ Apps        │
    │               │  │  Native)     │  │             │
    │ - GitHub      │  │              │  │ - Other     │
    │   webhooks    │  │ - Quantum    │  │   communities│
    │ - Leaderboard │  │   Sync       │  │ - DAOs      │
    │ - $Zo rewards │  │ - Bookings   │  │ - Coliving  │
    └───────────────┘  │ - Web3       │  │   spaces    │
                       │ - ZUI        │  └─────────────┘
                       └──────────────┘
```

**Key Integration Points:**

1. **Zo API (Auth Layer):** All services authenticate via phone OTP through Zo API

2. **Passport SDK (Reputation Layer):** 
   - Used by: zo.xyz apps, zohm, Builder Bot, Mobile App
   - Provides: Universal reputation, wallet, avatar, badges
   - Published on npm - any app can integrate

3. **Independent Services:**
   - **zo.xyz monorepo** - 9 Next.js apps (website landing, admin, pms, etc.)
   - **zohm** - Standalone questing/vibe score app
   - **Hospitality Bot** - Python microservice for housekeeping
   - **Builder Bot** - Telegram bot tracking GitHub contributions
   - **Mobile App** - React Native app with full feature set

4. **Data Flow Examples:**

**Contribution Flow:**
```
GitHub PR merged → Builder Bot (webhook) → Updates Passport SDK 
→ Reputation visible in: zo.xyz dashboard, zohm, Mobile App
```

**Hospitality Flow:**
```
WhatsApp message → Hospitality Bot (LangGraph routing) 
→ PMS query or task assignment → Response via WhatsApp
```

**Quest Flow:**
```
User completes quest in zohm → Earns $Zo → Updates Passport SDK 
→ Reputation + wallet balance shown in Mobile App
```

All six projects are **independent microservices** sharing:
- Zo API for authentication
- Passport SDK for reputation/identity
- REST APIs for cross-service communication

---

## The Structure

### Maintainers: The Dev Pod
**Who:** Core team (Samurai + dev pod: Manish, Omkar, and other core developers)

**Responsibilities:**
- Create and prioritize issues across all projects
- Review and merge pull requests
- Deploy approved features
- Set technical direction and code standards
- Manage $Zo token distribution
- Host weekly coordination calls
- Determine what counts as "code contribution" vs other contributions
- Manage and update the global leaderboard weekly

**Authority:** Final decision on what gets merged, deployed, and what counts toward the 11 code contribution threshold

---

### The 11: Elite Vibe Keepers (Rank #1-#11 on Leaderboard)
**Who:** The top 11 ranked contributors who also have 11+ code contributions

**Requirements:**
1. **Rank #1-#11** on the global performance leaderboard
2. **11+ code contributions** (features, architecture, complex fixes - validated by maintainers)

**Both Required:** If you rank #5 but only have 8 code contributions, you're in the 111 but NOT an elite vibe keeper yet. Ship 3 more code PRs!

**Highly Competitive:**
- Rankings update weekly based on recent velocity and quality
- Stop contributing → drop in ranking → lose elite vibe keeper status
- Other contributors can outrank you and take your top 11 spot
- Must continuously ship to maintain position

**Privileges:**
- Weekly Thursday 9 PM IST strategy calls (inner circle only)
- Direct input on roadmap and architectural decisions
- Maximum $Zo reward tier with elite multipliers
- Can propose and lead new initiatives
- Special "Elite Vibe Keeper" recognition
- Priority booking at all Zo Houses globally
- Direct collaboration with maintainers

**Commitment:** Keep shipping quality code to maintain your ranking. Inactive contributors drop fast.

---

### The 100: Leaderboard Hackers (Rank #12-#111)
**Who:** Contributors ranked 12-111 on the global leaderboard

**How to Enter:**
- Contribute quality code and other valuable work consistently
- Climb the rankings through velocity, quality, and impact
- Break into top 111 positions

**Leaderboard Ranking Factors:**
- Recent contribution velocity (last 3 months weighted heavily)
- Code quality and architectural significance
- PR review participation
- Community helpfulness and cultural fit
- Maintainers adjust rankings weekly

**Privileges:**
- Official recognition as part of the 111 elite hackers
- Listed on duh.zo live leaderboard with your rank (e.g., #23, #67, #104)
- Access to 111-only Telegram channel
- Can visit and work from Zo Houses
- Higher $Zo rewards than open contributors (scaled by rank)
- Voting rights on roadmap decisions
- **Path to Top 11:** Keep climbing + accumulate 11+ code contributions

**The Competition:**
- **Ranks #12-#50:** High-tier, significant $Zo bonuses
- **Ranks #51-#111:** Entry-tier, baseline elite benefits
- Drop below #111? You're out until you climb back up

**Your Rank Matters:** #12 earns more $Zo than #87. Competition is fierce.

---

### Open Contributors (Unlimited)
**Who:** Anyone building with us - no limit on participation

**How to Join:**
1. Browse open issues on any project  
2. Claim an issue you want to work on
3. Submit a pull request
4. Get it merged
5. Earn $Zo and climb the global leaderboard

**Your Journey:**
- **First PRs:** Welcome! Start building your ranking
- **Consistent Contributions:** Your rank starts showing up
- **Climb to #112-#200:** You're close to breaking into the 111
- **Break Top 111:** You're an elite hacker!
- **Climb to Top 11 + Hit 11 Code PRs:** Elite vibe keeper status unlocked

**Everyone Competes:**
- All contributors visible on global leaderboard
- Top 111 = elite status
- Top 11 (with 11+ code) = vibe keeper status
- It's transparent, competitive, meritocratic

---

### The Path to Elite Status

```
Open Contributor (anyone, ranked #500+)
    ↓
Ship quality PRs → Climb to #200
    ↓
Keep shipping → Break into top 111 (Elite Hacker status)
    ↓
Compete for top positions → Climb toward top 11
    ↓
Hit Rank #1-#11 + Accumulate 11+ Code PRs → Elite Vibe Keeper ✨
```

**One Leaderboard. Pure Competition. Top 111 are elite. Top 11 (with 11+ code) are vibe keepers.**

---

## How It Works

### The Contribution Flow

```
1. BROWSE ISSUES
   ↓ Pick an issue from any project
   
2. CLAIM & BUILD  
   ↓ Comment on issue to claim it
   ↓ Build your solution
   
3. SUBMIT PR
   ↓ Open pull request with your code
   
4. CODE REVIEW
   ↓ Maintainers review your work
   
5. GET MERGED
   ↓ PR gets merged into main branch
   
6. EARN REWARDS
   ↓ Receive $Zo tokens automatically
   ↓ Reputation increases in Zo Passport
   ↓ Builder Bot tracks your contribution
   
7. LEVEL UP
   ↓ Unlock new privileges
   ↓ Get invited to weekly calls
   ↓ Access Zo Houses
```

---

## The Weekly Cycle

### Monday: Issue Drop
- Maintainers post new issues across all projects
- Issues labeled by difficulty: `easy`, `medium`, `hard`, `epic`
- Clear requirements and acceptance criteria
- $Zo reward amount specified

### Monday-Friday: Build Time
- Contributors claim and work on issues
- Async collaboration in GitHub discussions
- Maintainers available for questions
- PRs can be submitted anytime

### Saturday-Wednesday: Review & Deploy
- Maintainers review all open PRs
- Merge approved contributions
- Test and deploy to staging
- Prepare for weekly call

### Thursday: The Weekly Call (60-90 min, 9 PM IST)
**Participants:** Maintainers + The 11 Elite Vibe Keepers (graduates with 11+ contributions)

**Time:** 9:00 PM IST (India Standard Time)
- 3:30 PM UTC
- 8:30 AM PST (Pacific Time)
- 11:30 AM EST (Eastern Time)
- 4:30 PM CET (Central European Time)

**Agenda:**
1. **Demos (30 min):** Contributors demo what they shipped
2. **Deploy (15 min):** Deploy approved features to production together
3. **Blockers (15 min):** Discuss technical challenges, get unstuck
4. **Planning (20 min):** Preview next week's priorities and big issues
5. **Community (10 min):** Shoutouts, announcements, coordination

**Format:**
- Recorded (for transparency)
- Async-friendly (summary posted for those who can't attend)
- Decision-making (quick calls on technical direction)

---

## $Zo Token Economics

### Token Purpose
$Zo is the reward and governance token for the Zo ecosystem, deployed on **Base L2 blockchain**. Contributors earn it by shipping code, and it represents both economic value and community reputation.

**Token Contract:** `0x111142c7ecaf39797b7865b82034269962142069`  
**Blockchain:** Base (Ethereum L2)  
**View on BaseScan:** https://basescan.org/token/0x111142c7ecaf39797b7865b82034269962142069

### Earning $Zo

**Issue Difficulty Rewards:**
- 🟢 **Easy (good-first-issue):** 50-100 $Zo
  - Documentation updates
  - UI/UX fixes
  - Simple bug fixes
  
- 🟡 **Medium:** 200-500 $Zo
  - New features
  - API integrations
  - Complex bug fixes
  
- 🔴 **Hard:** 500-1,500 $Zo
  - Architecture changes
  - Major features
  - System design work
  
- ⚫ **Epic:** 1,500-5,000 $Zo
  - Multi-week projects
  - New product launches
  - Infrastructure overhauls

**Bonus Multipliers:**
- **First-time contributor:** 1.5x on first merged PR
- **Weekly streak:** +10% per consecutive week
- **Code quality:** Up to 2x for exceptional work
- **Community help:** Bonus $Zo for helping others in discussions

### $Zo Utility

**Current:**
- Reputation building (tracked in Passport)
- Recognition within the community
- Future claim rights (mechanisms TBD)

**Planned:**
- Use at Zo Houses (stays, coworking, events)
- Trade with other contributors
- Governance voting on roadmap priorities
- Access to premium Zo services
- Revenue share from Zo ecosystem
- Early access to new city node launches

### Token Distribution

**How to Claim:** Multiple claiming mechanisms are being developed and will be announced. Options under consideration:
- Automatic distribution to wallet addresses on file
- Manual claim portal on zo.xyz
- Gradual vesting schedule
- Milestone-based unlocks

Stay tuned in the Telegram community for claiming mechanism announcements.

### Distribution Schedule
- **60%** - Contributor rewards (ongoing)
- **20%** - Core team and maintainers
- **10%** - Community treasury
- **10%** - Early supporters and partners

---

## Physical Nodes: Zo Houses

### The Network
Zo Houses are physical spaces where builders can live, work, and collaborate. Currently active nodes:

**Bangalore (Koramangala)** - Heritage house for founders
**Bangalore (Whitefield)** - Flagship HQ node  
**San Francisco** - Cultural prototype
**Bangkok** - Launching Q1 2025
**Dehradun** - Launching Q1 2025

### Access Levels

**Visitor:** 
- Anyone can visit for events and coworking
- Day passes available

**Builder (10+ merged PRs):**
- Can book short stays (1-7 days)
- Discounted rates with $Zo
- Access to builder events

**Core (50+ merged PRs):**
- Can live in houses long-term
- Priority booking
- Free coworking access
- Can host events and workshops

### Build Weeks
Monthly intensive sprints where contributors gather at a Zo House:
- Work on major features together
- Pair programming sessions
- Architecture planning
- Team bonding and culture building

---

## Reputation System: Zo Passport

Your Zo Passport is your identity across the ecosystem. It tracks:

### Contribution Metrics
- Total PRs merged
- Lines of code contributed
- Issues resolved
- Code review participation
- Community help (forum posts, mentoring)

### Reputation Score
A composite score based on:
- Quantity of contributions (20%)
- Quality of contributions (40%)
- Consistency (20%)
- Community impact (20%)

### Badges & Achievements
Unlock special recognition for milestones:
- 🌱 First Contribution
- 🔥 Weekly Warrior (5 weeks in a row)
- 🏗️ Architect (major system design)
- 🤝 Helper (assist 10+ contributors)
- 🏠 House Builder (contributed to all projects)
- ⭐ Core Contributor (50+ merged PRs)

---

## Getting Started

### For New Contributors

**Step 1: Join the Community**
- Join the Telegram community: https://t.me/duhzo
- Introduce yourself in the chat
- Star the repositories you're interested in
- Ask questions and get to know other builders

**Step 1b: Explore the Ecosystem**
- Browse zo.xyz to see the platform in action
- Check out the dashboard at app.zo.xyz (requires Zo Passport)
- Download the Zo Club app if you want to see the mobile experience
- Read the architecture docs in each repo's `/docs` folder
- Browse zo.xyz to see the platform in action
- Check out the /passport page to understand the reputation system
- Download the Zo World app if you have access
- Read the architecture docs in each repo's `/docs` folder

**Step 2: Set Up Your Development Environment**

**For Builder Bot (Python/Telegram):**
```bash
git clone https://github.com/ZoHouse/ZoBuilder-bot
cd ZoBuilder-bot
python3 -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your Telegram bot token, MongoDB URI, etc.
python bot.py
```

**For Hospitality Bot (Python/FastAPI):**
```bash
git clone https://github.com/ZoHouse/Hospitality-2.0
cd Hospitality-2.0
uv sync  # or pip install -r requirements.txt
cp .env.example .env
# Edit .env with Supabase, OpenAI, Groq, WhatsApp API keys
uvicorn app.main:app --reload --app-dir src
```

**For Passport SDK (TypeScript/npm):**
```bash
git clone https://github.com/ZoHouse/zopassport
cd zopassport
npm install
npm run dev
# Or create a test app:
npx create-zopassport
```

**For Zo Web Platform Monorepo (Next.js/Nx):**
```bash
git clone https://github.com/ZoHouse/zo.xyz
cd zo.xyz
yarn install
yarn nx serve website  # main landing page
# Or serve other apps: admin, dashboard, pms, payment, etc.
```

**For Zo World Questing Map (zohm):**
```bash
git clone https://github.com/ZoHouse/zohm
cd zohm
pnpm install  # or yarn/npm
pnpm dev
# Open http://localhost:3000
```

**For Zo Club Mobile App (React Native):**
```bash
git clone https://github.com/ZoHouse/ZoWorldmobile
cd ZoWorldmobile
yarn install
cd ios && pod install && cd ..  # iOS only
yarn ios  # or yarn android
```

**Step 3: Understand the Codebase**
- Watch the architecture walkthrough videos (pinned in each repo)
- Review the code structure and conventions
- Read through recent merged PRs to see coding patterns
- Ask questions in the #contributors channel

**Step 4: Find Your First Issue**
- Browse issues labeled `good-first-issue` 
- These are specifically chosen for onboarding
- Include clear requirements and context
- Usually take 2-4 hours for a first-time contributor

**Step 5: Claim & Build**
- Comment "I'd like to work on this" on the issue
- A maintainer will assign it to you
- Create a branch and build your solution
- Follow the contribution guidelines in CONTRIBUTING.md

**Step 6: Submit Your PR**
- Open a pull request with a clear description
- Reference the issue number (#123)
- Include screenshots/videos for UI changes
- All tests must pass
- A maintainer will review within 48 hours

**Step 7: Earn & Level Up**
- Once merged, Builder Bot automatically awards $Zo
- Your reputation increases in Zo Passport
- Your contribution appears in weekly leaderboards
- Start working towards your next level

---

### For Experienced Contributors

If you're already a seasoned open source developer:

**High-Impact Areas:**
- **Architecture improvements** - Refactor existing systems for scale
- **Performance optimization** - Speed up slow queries and renders
- **AI/LangGraph development** - Build new personas and workflows for Hospitality Bot
- **Testing infrastructure** - Add comprehensive test coverage
- **Documentation** - Write guides for complex features
- **New integrations** - Connect to external APIs and services (PMS, WhatsApp, etc.)
- **Mobile development** - Improve Zo World app
- **SDK expansion** - Build Passport integrations for other languages
- **Python backend** - Work on FastAPI microservices

**Ways to Contribute Beyond Code:**
- Review other contributors' PRs
- Mentor new contributors in Discord
- Write technical blog posts about the architecture
- Propose major feature additions
- Lead discussion on technical decisions

---

### Example Issues by Project

To help you understand what kinds of contributions we need, here are real examples:

**Zo Web Platform Monorepo (zo.xyz):**
- `[monorepo/website]` Improve landing page hero section - 400 $Zo
- `[monorepo/dashboard]` Add Vibe Score widget to home screen - 500 $Zo
- `[monorepo/pms]` Build recurring task scheduler for property management - 600 $Zo
- `[monorepo/admin]` Create analytics dashboard for house occupancy - 800 $Zo
- `[monorepo/payment]` Add support for new payment gateway - 700 $Zo
- `[monorepo/web-checkin]` Implement QR code self-check-in - 600 $Zo
- `[monorepo/shared]` Create new reusable component in @zo/moal - 400 $Zo
- `[monorepo/ops-backend]` Add new Express API endpoint - 500 $Zo
- `[monorepo/infra]` Optimize AWS ECS deployment pipeline - 1,000 $Zo

**Zo World Questing Map (zohm):**
- `[zohm/quests]` Add new quest type (physical location challenge) - 800 $Zo
- `[zohm/vibe-score]` Improve vibe score algorithm with new factors - 1,000 $Zo
- `[zohm/map]` Add 3D building models to node visualization - 1,200 $Zo
- `[zohm/passport]` Create new badge designs for achievements - 500 $Zo
- `[zohm/quantum-sync]` Improve voice analysis accuracy - 900 $Zo
- `[zohm/culture]` Add new culture categories and icons - 400 $Zo
- `[zohm/narrative]` Build AI narrative generation for quest completion - 1,500 $Zo
- `[zohm/nodes]` Add Zostel network integration (50+ locations) - 1,000 $Zo

**Hospitality 2.0 Bot (Python/FastAPI):**
- `[bot/agent]` Add new persona for maintenance staff - 1,500 $Zo
- `[bot/agent]` Improve intent detection with more keywords - 400 $Zo
- `[bot/pms]` Add support for additional PMS platforms - 1,200 $Zo
- `[bot/whatsapp]` Add voice message support - 800 $Zo
- `[bot/analytics]` Build efficiency dashboard for staff performance - 1,000 $Zo
- `[bot/tasks]` Create smart task assignment algorithm based on staff skills - 1,500 $Zo
- `[bot/zones]` Add new property zones (garden, rooftop, etc.) - 300 $Zo
- `[bot/langgraph]` Implement multi-turn conversation memory - 900 $Zo
- `[bot/integration]` Connect to Passport SDK for staff reputation - 700 $Zo
- `[bot/tests]` Add comprehensive pytest coverage for personas - 600 $Zo

**Zo Passport SDK (npm: zopassport):**
- `[sdk]` Add Base (L2) blockchain wallet integration - 1,000 $Zo
- `[sdk]` Add Ethereum mainnet wallet support - 1,000 $Zo
- `[sdk]` Build Python SDK wrapper for backend services - 1,200 $Zo
- `[sdk]` Build Go SDK wrapper for backend services - 1,200 $Zo
- `[sdk]` Build Ruby SDK wrapper for Rails apps - 1,000 $Zo
- `[sdk]` Add webhook support for real-time reputation updates - 800 $Zo
- `[sdk]` Write "Integrating Passport in Next.js" tutorial - 300 $Zo
- `[sdk]` Write "Integrating Passport in React Native" tutorial - 300 $Zo
- `[sdk]` Create VS Code extension for SDK development - 1,500 $Zo
- `[sdk]` Improve avatar generation API (faster polling, better quality) - 700 $Zo
- `[sdk]` Add support for custom passport card themes - 600 $Zo

**Zo Club Mobile App (React Native):**
- `[mobile/quantum-sync]` Improve audio recording quality and compression - 600 $Zo
- `[mobile/quantum-sync]` Add new quest types beyond audio challenges - 800 $Zo
- `[mobile/bookings]` Implement calendar-based room availability view - 700 $Zo
- `[mobile/bookings]` Add workstation day-use booking flow - 500 $Zo
- `[mobile/zui]` Create new reusable component in ZUI design system - 400 $Zo
- `[mobile/web3]` Add support for new blockchain (Optimism, zkSync) - 1,000 $Zo
- `[mobile/chat]` Implement voice messages in Socket.io chat - 600 $Zo
- `[mobile/passport]` Build animated passport card transitions - 500 $Zo
- `[mobile/performance]` Optimize app bundle size (reduce by 30%) - 800 $Zo
- `[mobile/icons]` Add new app icon theme (10th design) - 300 $Zo

**Zo Builder Bot (Telegram + Python):**
- `[bot]` Add GitLab webhook support for tracking contributions - 700 $Zo
- `[bot]` Add Bitbucket webhook support - 600 $Zo
- `[bot]` Build weekly contribution digest with charts and visualizations - 500 $Zo
- `[bot]` Create interactive leaderboard with wallet addresses - 600 $Zo
- `[bot]` Improve Builder Score algorithm (more factors, better weighting) - 800 $Zo
- `[bot]` Add `/projects` command to list active Zo projects - 300 $Zo
- `[bot]` Add `/quest` command to assign contribution quests - 700 $Zo
- `[bot]` Integrate with Passport SDK for unified reputation - 1,000 $Zo
- `[bot]` Build admin dashboard for managing scores and rewards - 1,200 $Zo
- `[bot]` Add automatic $Zo token distribution on PR merge - 1,500 $Zo

**Cross-Project:**
- `[all]` Create unified API documentation site - 1,500 $Zo
- `[all]` Build E2E testing suite covering all projects - 2,000 $Zo
- `[all]` Set up monitoring and alerting infrastructure - 1,200 $Zo
- `[all]` Write architecture decision records (ADRs) - 400 $Zo

---

### Understanding the Existing Codebase

Since these projects are already built and running, here's what to expect:

**What's Already Done:**
- **Monorepo Infrastructure**: Nx 17.1.3 workspace with 9 production apps + shared libraries
- **Authentication**: Phone OTP via Zo API across all platforms
- **Passport SDK**: Published on npm as `zopassport`, React + React Native components
- **Mobile App**: Full React Native app with 39 screens, Web3, Quantum Sync, bookings
- **Hospitality Bot**: LangGraph agentic system with 18+ zones, WhatsApp integration, PMS automation
- **Builder Bot**: Telegram bot with GitHub webhooks, Builder Score, leaderboards
- **Database Schemas**: PostgreSQL (Supabase) for most services, MongoDB for Builder Bot
- **Deployment Pipelines**: AWS ECS for monorepo, production-ready mobile app
- **Component Libraries**: ZUI Design System (100+ components), @zo shared libraries
- **API Layer**: 130+ API endpoints via @zo/auth
- **Real-time Features**: Socket.io chat, Supabase subscriptions
- **Web3 Integration**: WalletConnect v2, multi-chain support, NFT gallery
- **AI/ML**: LangGraph personas, AssemblyAI voice analysis, OpenAI integrations

**What Needs Work:**
- Feature expansion (new capabilities)
- Performance optimization (faster, more efficient)
- UI/UX improvements (better user experience)
- Testing coverage (more comprehensive tests)
- Documentation (architecture guides, API docs)
- Bug fixes (things that don't work quite right)
- Refactoring (improving code quality)

**Technical Debt to Tackle:**
Each repo has a `TECHNICAL_DEBT.md` file listing known issues:
- Areas needing refactoring
- Performance bottlenecks
- Missing test coverage
- Documentation gaps
- Deprecated dependencies

---

## Technical Standards

### Code Quality Requirements
- Clean, readable code with clear variable names
- Comments for complex logic
- Follows project style guides (enforced by linters)
- No breaking changes without discussion
- Tests for new features (when applicable)

### PR Guidelines
- One feature or fix per PR
- Clear description of what and why
- Screenshots/videos for UI changes
- Links to related issues
- Passing CI/CD checks

### Communication
- Be respectful and constructive
- Ask questions early and often
- Document decisions in GitHub discussions
- Keep maintainers updated on blockers
- Celebrate others' contributions

---

## Roadmap

### Phase 0: Pre-Launch Preparation (Week 0)
**CRITICAL:** Before opening repositories to external contributors, ensure:

**Code Hygiene:**
- [ ] Remove all API keys, secrets, and credentials
- [ ] Review code for any sensitive business logic
- [ ] Clean up commented-out code and debug statements
- [ ] Ensure consistent code style across files
- [ ] Remove any internal/private references

**Documentation:**
- [ ] README.md with clear project description
- [ ] CONTRIBUTING.md with setup instructions
- [ ] DEVELOPMENT.md with local dev environment setup
- [ ] ARCHITECTURE.md explaining system design
- [ ] API.md documenting all endpoints (if applicable)
- [ ] CODE_OF_CONDUCT.md for community standards

**Infrastructure:**
- [ ] Set up separate staging environment for contributors
- [ ] Configure CI/CD to run on external PRs
- [ ] Create public issue templates
- [ ] Set up branch protection rules
- [ ] Prepare demo/sandbox environment

**Issue Backlog:**
- [ ] Create 10+ good-first-issue tasks
- [ ] Label existing issues by difficulty
- [ ] Write clear acceptance criteria for each issue
- [ ] Assign $Zo reward amounts
- [ ] Organize by feature area

**Legal & Licensing:**
- [ ] Choose open source license (MIT recommended)
- [ ] Add LICENSE file to each repo
- [ ] Ensure no dependencies with incompatible licenses
- [ ] Contributor License Agreement (if needed)

---

### Phase 1: Open Source Launch (Month 1-2)
**Goal:** Prepare existing codebases for external contributors and onboard first wave of builders

**Week 1: Open Source Launch (Days 1-7)**
- ✅ Clean up Builder Bot codebase (remove secrets, add docs)
- ✅ Create CONTRIBUTING.md and setup guide
- ✅ Document MongoDB schema and GitHub webhook setup
- ✅ Create 20 good-first-issue tasks
- ✅ Set up $Zo reward structure
- ✅ Launch Builder Bot as first open source project
- 🎯 Goal: 10-15 contributors, first PRs merged

**Week 2: Passport SDK Expansion (Days 8-14)**
- ✅ Publish SDK documentation site
- ✅ Create Python SDK wrapper starter
- ✅ Create 15 SDK-related issues (wrappers, integrations, docs)
- ✅ Open source example integrations (Next.js, React Native)
- 🎯 Goal: 20-30 total contributors, first SDK wrapper PR

**Week 3: Hospitality Bot Launch (Days 15-21)**
- ✅ Clean up Hospitality Bot (LangGraph workflows, env setup)
- ✅ Document persona system and zone management
- ✅ Create 20 issues (new personas, PMS integrations, analytics)
- ✅ Open source the Python/FastAPI codebase
- 🎯 Goal: 40-50 contributors, Python devs joining

**Week 4: Monorepo Apps (Days 22-30)**
- ✅ Choose 2-3 apps from monorepo to open source (dashboard, meme, comic)
- ✅ Extract from monorepo or open entire repo (decision TBD)
- ✅ Document Nx workspace setup and shared libraries
- ✅ Create 25+ issues across multiple apps
- 🎯 Goal: 60-80 contributors, first weekly call with 11 active builders

**Month 2: Mobile App & Full Stack (Days 31-60)**
- ✅ Open source Zo Club mobile app
- ✅ Open remaining monorepo apps
- ✅ Create comprehensive contribution guide for all stacks
- 🎯 Goal: 100+ contributors, self-sustaining PR flow

---

### Phase 2: Momentum & Feature Development (Month 3-4)
**Goal:** Establish consistent contribution cadence and ship major features

**Projects:**
- Passport SDK v2 with multi-chain support
- Mobile app feature parity with web platform
- Builder Bot advanced analytics dashboard
- Hospitality 2.0 agent improvements
- Game platform quest designer tool

**Milestones:**
- First build week at Zo House Bangalore
- 10+ external contributors with merged PRs
- Documentation site launch (docs.zo.xyz)
- First external integration of Passport SDK
- 🎯 Target: 40-60 active contributors

**Community:**
- Weekly calls consistently have 11 active participants
- Community-led feature proposals emerge
- First contributor-organized hackathon
- Mentor program for new contributors

---

### Phase 3: Scale & External Adoption (Month 5-6)
**Goal:** Fill the 111 elite hacker leaderboard and establish competitive top 11

**Products:**
- All 6 projects fully operational with external contributors
- Passport SDK adopted by 2+ external communities
- Mobile app v2 with advanced features
- Builder Bot multi-platform support (GitLab, Bitbucket)
- Questing map (zohm) used by external communities

**Ecosystem:**
- Bangkok and Dehradun Zo Houses activated
- Monthly build weeks rotating across cities
- Advanced reputation system with governance
- Revenue share model for contributors
- 🎯 Target: 150+ open contributors, 111 elite hacker leaderboard full and competitive, 8-11 people consistently in top 11 with code threshold met

**Governance:**
- Core contributor elections
- Roadmap voting with $Zo
- Feature bounty program
- Technical steering committee formed

---

### Phase 4: Network Effects & Sustainability (Month 7-12)
**Goal:** Become the standard infrastructure for networked communities

**Adoption:**
- Zo tools powering 10+ external communities
- Passport SDK with 1,000+ monthly active users
- Multiple language SDKs (Python, Go, Ruby)
- Enterprise licensing model
- Open core business model established

**Community:**
- International contributor meetups
- duh.zo conference
- **Top 111 leaderboard** highly competitive and prestigious
- **Top 11 elite vibe keepers** consistently maintained by active core contributors
- Self-sustaining contribution economy
- 🎯 Target: Revenue-positive, 250+ open contributors, fierce competition for all 111 elite spots

**Impact:**
- Case studies from external adopters
- Research papers on networked community infrastructure
- Partnerships with major coliving networks
- Foundation established for long-term governance

---

## Why Build With Us

### For Hackers
- **Real impact:** Your code runs in actual physical spaces used by real people
- **Token rewards:** Get compensated for open source work
- **Global network:** Access to Zo Houses in multiple cities
- **Elite community:** Work alongside the best builders
- **Own what you build:** $Zo gives you ownership in the ecosystem
- **Learn by doing:** Contribute to cutting-edge tech (AI agents, IoT, crypto)

### For the Ecosystem
- **Open source first:** All code is public and forkable
- **Modular design:** Use individual tools or the full stack
- **Battle-tested:** Built for real operations, not just demos
- **Community-driven:** Roadmap shaped by contributors
- **Token-aligned:** Everyone who builds owns a piece

---

## Principles

### Technical Principles
1. **Ship fast, iterate faster** - Bias toward action over perfection
2. **Modularity over monoliths** - Each tool should work independently
3. **Documentation is code** - If it's not documented, it doesn't exist
4. **Async-first** - Support global contributors across time zones
5. **Test in production** - Real Zo Houses are our proving ground

### Community Principles
1. **Contribution over credentials** - Your code speaks louder than your resume
2. **Teach while you learn** - Help others level up
3. **Feedback is a gift** - Give it early, often, and kindly
4. **Transparency by default** - Open roadmap, open metrics, open discussions
5. **No assholes** - Skill matters, but so does how you treat people

### Operational Principles
1. **Dogfood everything** - We use what we build
2. **Data-driven decisions** - Measure what matters
3. **Sustainable pace** - No burnout culture
4. **Distributed authority** - Maintainers guide, contributors decide
5. **Long-term thinking** - Building for decades, not quarters

---

## The Passport SDK: Our Strategic Differentiator

### Why Passport SDK Matters

While the web platform, mobile app, and bot are valuable for running Zo Houses, **the Passport SDK is what makes this ecosystem composable and scalable beyond our own network.**

**The Insight:** Reputation should be portable, not siloed.

Traditional platforms lock your reputation in their walled garden:
- Your GitHub stars don't transfer to GitLab
- Your Reddit karma doesn't help on StackOverflow  
- Your Twitter followers don't matter on LinkedIn

**Zo Passport breaks this model:** Your contributions follow you everywhere.

---

### How External Communities Can Use It

**Scenario 1: Another Coliving Network**
```javascript
// A coliving space in Berlin integrates Passport
import { ZoPassport } from 'zo-passport-sdk'

const passport = new ZoPassport({ apiKey: 'their-key' })

// Check if member has verified reputation
const member = await passport.getReputation('user-123')

if (member.score > 500) {
  // Auto-approve for long-term stay
  await bookingSystem.approve(member)
}
```

**Scenario 2: A DAO Tracking Contributors**
```javascript
// DAO uses Passport to track who's actually building
const contributors = await passport.listContributors({
  minScore: 100,
  badges: ['core-contributor', 'weekly-warrior']
})

// Airdrop governance tokens to proven builders
contributors.forEach(c => {
  daoContract.airdrop(c.walletAddress, c.score * 10)
})
```

**Scenario 3: A Hackathon Verifying Participants**
```javascript
// Hackathon verifies hacker credentials
const hacker = await passport.getReputation(userId)

if (hacker.badges.includes('first-contribution')) {
  // Beginner track
} else if (hacker.prsCompleted > 50) {
  // Advanced track
}
```

---

### Network Effects

The more apps integrate Passport, the more valuable it becomes:

```
10 apps → Your reputation matters in 10 places
100 apps → Your reputation becomes your professional identity
1,000 apps → Passport is the LinkedIn for builders
```

**This is the moat:** Once someone has earned reputation in Passport, they'll want to use it everywhere. Once apps integrate Passport, they tap into an existing network of verified builders.

---

### SDK Adoption Strategy

**Year 1 (Internal):**
- Perfect the SDK within Zo ecosystem
- All 4 Zo projects use it seamlessly
- Prove it works at scale with real users

**Year 2 (Friendly Networks):**
- Integrate with 5-10 friendly coliving spaces
- Partner with hacker houses globally
- Build case studies showing impact

**Year 3 (Open Market):**
- Major DAO platforms integrate it
- Developer tools adopt it (GitLab, Bitbucket)
- Enterprise clients license it
- Passport becomes a standard

---

### Why Contributors Should Focus on SDK

**For the community:**
- Most strategic long-term project
- Attracts sophisticated developers
- Creates defensible network effects

**For individual contributors:**
- Learn to build developer tools
- Most portable skill (SDK design)
- Highest visibility (other devs use your work)
- Best for resume/portfolio

**High-Impact SDK Issues:**
- Adding blockchain integrations (Solana, Base, Arbitrum)
- Building language-specific wrappers (Python, Go, Ruby)
- Creating developer tools (CLI, VS Code extension)
- Writing comprehensive docs and examples
- Building a playground for testing

---

## Frequently Asked Questions

**Q: Do I need to live in a Zo House to contribute?**  
A: No! Most contributors work remotely. Houses are available for those who want to visit or live there.

**Q: What if I can't make the weekly call?**  
A: Calls are recorded and summarized. Participation is encouraged but not required.

**Q: How much time do I need to commit?**  
A: None. Contribute as much or as little as you want. Even one PR counts.

**Q: What tech stack are you using?**  
A: We use a microservices architecture with modern, production-ready stacks:
- **Zo Web Platform** (Monorepo): Next.js 14, React 18, TypeScript, Nx 17.1.3, Tailwind CSS, Ant Design, MUI, PostgreSQL, Redis, AWS ECS
- **Hospitality 2.0 Bot**: Python 3.11+, FastAPI, LangGraph (OpenAI + Groq), PostgreSQL (Supabase), Playwright, WhatsApp APIs
- **Zo Passport SDK** (npm: `zopassport`): TypeScript, React, React Native, react-native-web, with planned wrappers for Python, Go, Ruby
- **Zo World Mobile App** (Zo Club): React Native 0.73.6, TypeScript, Native Base, TanStack Query, WalletConnect v2, Firebase, Socket.io
- **Zo Builder Bot** (Telegram): Python 3.8+, python-telegram-bot, FastAPI (webhooks), MongoDB, GitHub webhooks

All projects use TypeScript/Python for type safety and modern tooling.

**Q: Can I contribute to multiple projects?**  
A: Absolutely! In fact, we encourage it. Understanding how the projects connect makes you more effective.

**Q: What if my PR gets rejected?**  
A: Maintainers will provide feedback. Revise and resubmit, or try a different issue. Rejected PRs are a learning opportunity.

**Q: Is there a minimum skill level required?**  
A: We have issues for all skill levels. Start with `good-first-issue` if you're new to the codebase.

**Q: How do I cash out $Zo tokens?**  
A: $Zo is deployed on Base L2 (Ethereum Layer 2). Token contract: `0x111142c7ecaf39797b7865b82034269962142069`. Multiple claiming mechanisms are under development - announcements will be made in the Telegram community. Once claimed to your wallet, you can trade on Base-compatible DEXs or hold for future utility within the Zo ecosystem.

**Q: Can I join The 11 (Elite Vibe Keepers)?**  
A: Two requirements: (1) Rank #1-#11 on the global leaderboard, AND (2) Have at least 11 code contributions (features/architecture/complex fixes - validated by maintainers). Rankings update weekly based on performance, so you must keep contributing to maintain your top 11 position.

**Q: What's the difference between The 11 and The 100?**  
A: 
- **The 11** = Ranks #1-#11 on the leaderboard (must also have 11+ code contributions for elite vibe keeper status)
- **The 100** = Ranks #12-#111 on the leaderboard
- It's one continuous leaderboard - everyone ranked #1-#111 are elite hackers

**Q: What if I rank #5 but only have 8 code contributions?**  
A: You're in the 111 elite hackers and get most benefits (Telegram access, $Zo bonuses, voting rights), but you don't get "Elite Vibe Keeper" status (weekly calls, max rewards) until you hit 11 code contributions. Ship 3 more code PRs and you'll unlock it!

**Q: Is The 11 permanent or do I have to maintain my rank?**  
A: You must maintain your rank! The leaderboard is competitive and updates weekly. If you stop contributing and others outrank you, you drop out of the top 11. Keep shipping to keep your elite vibe keeper status.

**Q: Can I use these tools for my own community?**  
A: Yes! Everything is open source. Fork it, use it, improve it. We'd love to see what you build.

**Q: These projects are already in production - what if I break something?**  
A: We have staging environments and comprehensive testing. All PRs must pass CI/CD before merging. Critical changes get extra review.

**Q: How do I know what's safe to change?**  
A: Issues are labeled with risk level. Start with low-risk tasks. Ask maintainers before touching core systems.

**Q: What if there's a bug in production?**  
A: Critical bugs get priority. Tag issues with `urgent` and notify maintainers in Discord. Hotfix PRs are fast-tracked.

**Q: How does code review work?**  
A: Maintainers review all PRs within 48 hours. For major changes, multiple maintainers review. You'll get constructive feedback.

**Q: Can I refactor existing code?**  
A: Yes, but discuss with maintainers first. Refactoring PRs need strong justification and must maintain backward compatibility.

**Q: What if I disagree with architectural decisions?**  
A: Open a GitHub Discussion to propose alternatives. Bring data and examples. The community debates and maintainers decide.

---

## Contact & Links

**Community Site:** duh.zo  
**Main Platform:** zo.xyz  
**Telegram Community:** https://t.me/duhzo

**GitHub Organization:** github.com/ZoHouse
- `zo.xyz` - Web platform monorepo (9 Next.js apps including main landing)
- `zohm` - Zo World questing map (vibe score, quests, node visualization)
- `Hospitality-2.0` - Housekeeping automation (Python/FastAPI/LangGraph)
- `ZoBuilder-bot` - Telegram bot for tracking contributions
- `zopassport` - Passport SDK (npm package)
- `ZoWorldmobile` - Zo Club mobile app (React Native)

**Twitter:** [TO BE FILLED]  
**Email:** builders@duh.zo

**Weekly Call:** Every Thursday, 9:00 PM IST (3:30 PM UTC)  
**Meeting Link:** [TO BE FILLED - Zoom/Google Meet/Discord]

---

## Join Us

**duh.zo** is just beginning. We're looking for hackers who want to:
- Build something that matters in the real world
- Own a piece of what they create  
- Work with elite builders globally
- Shape the future of how humans coordinate

**The Path:**
1. **Start contributing** - Pick an issue, ship a PR, get on the leaderboard
2. **Climb the rankings** - Quality contributions move you up the global leaderboard (updated weekly)
3. **Break into top 111** - Elite hacker status unlocked
4. **Fight for top 11** - Rank #1-#11 + accumulate 11+ code contributions = elite vibe keeper

**Pure Competition:**
- One global leaderboard ranks everyone
- Top 111 = elite hackers
- Top 11 (with 11+ code) = vibe keepers
- Your rank determines your rewards

If this resonates, pick an issue and ship your first PR.

**Welcome to duh.zo.**

---

*This is a living document. Last updated: December 2024*  
*Contribute improvements to this doc by opening a PR at [LINK]*
