# UI/UX Website Redesign Agent Prompt

## Objective

Redesign the current website into a highly polished, content-focused minimalist blog tailored for a software engineer who cycles. The design must feel clean, modern, hyper-readable, and fast.

## Color Palette Tokens

Apply these exact Tailwind CSS arbitrary values or configure them in the Tailwind config theme extension:

- **Dominant Background:** `#F8FAFC` (Slate 50) - Clean, premium off-white that prevents eye strain.
- **Secondary / Text & Structure:** `#334155` (Slate 700) - Soft dark slate used for high-contrast typography, structural borders, and body text.
- **Accent:** `#ADFF2F` (Green-Yellow / Electric Lime) - Used sparingly and deliberately for focus states, call-to-action highlights, and subtle interactive anchor elements.

## Design Philosophy & System Rules

1. **Ruthless Minimalism:** Eliminate all unnecessary cards, drop shadows, background gradients, and complex decoration. Use ample whitespace (`px-6 py-12 md:py-24`) to give elements breathing room.
2. **Typography Scale:** Implement a strict typographic hierarchy using a clean sans-serif stack (e.g., Inter, Geist, or system-sans).
   - Section Headings: Medium weight, low tracking (`tracking-tight`), in the Secondary color.
   - Body Copy: Leading-relaxed (`leading-relaxed`) for absolute ease of reading.
3. **Intentional Accents:** The accent color `#ADFF2F` is highly vibrant. **Never** use it for large background sections or text blocks. Use it only for:
   - Hover active states (e.g., an underline text decoration or background fill transition on buttons).
   - Small custom badges or bullet point icons inside article highlights.

## Layout Components & Blueprint

### 1. Navigation Header

- **Layout:** A sticky, transparent, or solid `#F8FAFC` clean header bar with a thin bottom border (`border-b border-slate-200`).
- **Elements:** Minimal text logo on the left (`The Cycling Dev`), and raw text navigation links on the right (Blog, About, Projects) using the Secondary color.
- **Interactive State:** Hovering over nav links should trigger a subtle accent color indicator.

### 2. Homepage Hero Section

- **Layout:** A single-column text layout centered or left-aligned with maximum whitespace. No heavy images or complex graphics.
- **Typography:** Large, bold headline detailing the crossover between engineering and cycling.
- **Call to Action:** A sleek button with a Secondary color solid background and white text, shifting to an Accent colored border or indicator on focus.

### 3. Blog List Grid / Typography Layout

- **Layout:** A clean, vertical stack layout rather than dense grids. Each post entry displays the publication date in a muted gray text, followed by a bold article title that transitions cleanly on hover.
- **UX Touch:** Ensure target touch areas are at least 48px for mobile users reading on the go.

### 4. Article Presentation Page (Post Template)

- **Layout:** A tight, centered 65ch max-width reading column (`max-w-2xl mx-auto`) to optimize text scanning and minimize reader fatigue.
- **Affiliate/Callout Disclaimers:** Style callout containers using a subtle border (`border-l-4 border-slate-300`) with a very light background fill.

## Execution Output Requirements

Generate the layout adjustments inside the primary Astro layout structures (`src/layouts/`, `src/components/`, and `src/pages/index.astro`). Ensure all code utilizes class utilities native to Tailwind CSS. Maintain absolute component separation and avoid nested logic pollution.
