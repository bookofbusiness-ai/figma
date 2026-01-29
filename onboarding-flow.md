# BookofBusiness.ai — Onboarding Flow

Multi-step wizard that guides new customers from signup to their first workspace. Modeled after Figma's own onboarding pattern: dark theme, progress bar, single-question-per-step.

---

## Global Layout

- **Background:** Dark gray (#1E1E1E)
- **Content area:** Centered, max-width 600px
- **Top bar:** Back arrow (left), Language selector (right) — hidden on Step 1
- **Bottom bar:** Progress bar (left), Continue button (right, blue #3B82F6)
- **Typography:** White (#FFFFFF) headings, gray (#9CA3AF) subtitles
- **Selected state:** Blue border (#3B82F6) + light blue fill (#3B82F6/15%)
- **Unselected state:** Gray border (#4B5563) + transparent fill

---

## Step 1: Your Name

**Progress:** 20%

### Heading
> What's your name?

### Subtitle
> This is what others see when you join your team workspace.

### Content
- **Text input** — placeholder: "Your full name", pre-filled if available from signup
- **Live preview panel** (right side on desktop, hidden on mobile):
  - Shows a mock workspace header with the user's name
  - Label: "[Name]'s Workspace" with a Pro badge
  - User avatar circle (top-right corner)

### Behavior
- Continue button disabled until name has 2+ characters
- No back arrow on this step

---

## Step 2: Business Type

**Progress:** 40%

### Heading
> What kind of business do you run?

### Subtitle
> This helps us tailor your AI agents and templates.

### Options (single-select chips, 2 rows)
Row 1:
- Sales Team
- Marketing Agency
- Consulting Firm
- Real Estate

Row 2:
- Solo Entrepreneur
- Something else

### Behavior
- One selection required to continue
- "Something else" shows a text input below the chips

---

## Step 3: Your Role

**Progress:** 60%

### Heading
> Which role best describes you?

### Subtitle
> If you wear many hats, pick what you do most often.

### Options (single-select chip grid, 3 columns)
Row 1:
- Sales Rep
- Sales Manager
- VP of Sales

Row 2:
- Marketing
- Founder / CEO
- Operations

Row 3:
- Account Executive
- BDR / SDR
- Other

### Behavior
- One selection required to continue
- "Other" shows a text input below the chips

---

## Step 4: Choose Your Plan

**Progress:** 80%

### Heading (centered)
> Which plan would you like?

### Plan Cards (3 columns, radio-select)

#### Starter
- **Subtitle:** Best for solopreneurs getting started with AI
- **Price:** $99/mo
- **Features:**
  - 1 custom AI agent
  - Branded website or landing pages
  - 24/7 automated operations
  - Email & text outreach
  - Lead capture & qualification
  - Calendar integration
  - Weekly performance reports
  - Email support

#### Growth — "Most popular" badge
- **Subtitle:** Best for growing teams that need more firepower
- **Price:** $149/mo
- **Features:**
  - Everything in Starter, plus:
  - 2 custom AI agents
  - CRM integration
  - Advanced analytics dashboard
  - Priority support
  - A/B testing campaigns
  - Custom reporting

#### Enterprise
- **Subtitle:** Best for teams that need full AI coverage
- **Price:** $299/mo
- **Features:**
  - Everything in Growth, plus:
  - Unlimited AI agents
  - Dedicated account manager
  - Custom integrations
  - SLA guarantee
  - Team training & onboarding
  - API access

### Behavior
- Growth pre-selected by default
- Radio button top-right of each card
- Selected card has blue border + lighter background

---

## Step 5: Set Up Your Workspace

**Progress:** 100%

### Heading
> Name your workspace

### Subtitle
> You can always change this later in settings.

### Content
- **Text input** — placeholder: "e.g. Acme Sales Team", auto-filled as "[Name]'s Workspace"
- **Invite section** (below, optional):
  - Label: "Invite teammates (optional)"
  - Email input with "+" button to add more
  - Ghost text: "colleague@company.com"

### Behavior
- Workspace name required (pre-filled)
- Invites are optional — can skip
- Continue button text changes to "Launch Workspace"
- On submit: creates workspace, redirects to dashboard

---

## Responsive Notes

- **Desktop (>1024px):** Step 1 shows live preview panel on the right. Plan cards display as 3 columns.
- **Tablet (768–1024px):** Preview panel hidden. Plan cards stack to 2 columns + 1.
- **Mobile (<768px):** Full-width single column. Plan cards stack vertically. Chips wrap naturally.
