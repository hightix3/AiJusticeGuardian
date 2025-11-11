# AI Justice Guardian - Design Guidelines

## Design Approach

**System**: Enterprise Design System (Fluent/Carbon-inspired)
**Rationale**: Legal platform requiring trust, data clarity, and professional credibility. Information-dense interface with complex workflows demands systematic consistency.

## Typography

**Font Families**:
- Primary: Inter (via Google Fonts CDN) - clean, professional, excellent readability
- Monospace: JetBrains Mono - for case numbers, transaction IDs, data fields

**Hierarchy**:
- Page Titles: text-4xl font-bold
- Section Headers: text-2xl font-semibold
- Card Titles: text-xl font-semibold
- Body Text: text-base font-normal
- Captions/Meta: text-sm font-medium
- Data Labels: text-xs font-medium uppercase tracking-wide

## Layout System

**Spacing Primitives**: Tailwind units of 4, 6, 8, 12, 16
- Component padding: p-6 to p-8
- Section margins: my-12 to my-16
- Card gaps: gap-6
- Element spacing: space-y-4

**Grid Structure**:
- Dashboard: 3-column grid (lg:grid-cols-3) for metrics
- Case cards: 2-column (md:grid-cols-2)
- Main content: max-w-7xl mx-auto px-6

## Component Library

### Navigation
- Top navigation bar with logo, main menu, user profile
- Sticky sidebar for dashboard navigation (w-64)
- Breadcrumbs for deep navigation paths

### Hero Section
- Professional hero with large background image showing justice/legal imagery (courthouse, scales of justice, or abstract professional photography)
- Overlaid headline + subtitle with blurred-background buttons
- Height: min-h-[600px]
- Include trust indicators below hero (stats: "500+ Cases Resolved", "₩2.5B Recovered")

### Data Display
- **Metric Cards**: Elevated cards (shadow-lg) with large numbers, labels, trend indicators
- **Case Cards**: Comprehensive cards with status badges, timeline, key data points, action buttons
- **Tables**: Striped rows, sortable headers, sticky column headers for long lists
- **Progress Trackers**: Step-by-step visual indicators showing investigation stages

### Forms & Inputs
- **Case Submission Form**: Multi-step wizard layout
- Input fields: Large touch targets (h-12), clear labels above inputs
- File upload: Drag-and-drop zones with preview thumbnails
- Validation: Inline error states with helpful messages

### Status Indicators
- Badge system: Compact rounded badges for case status (In Progress, Under Review, Resolved, Funds Recovered)
- Color-coded but using patterns/icons for accessibility

### Data Visualization
- **Fund Flow Diagrams**: Visual representation of money movement
- **Timeline Views**: Horizontal scrolling timeline for case events
- **Charts**: Simple bar/line charts for statistics (use Chart.js via CDN)

### Action Buttons
- Primary CTA: Large, prominent (px-8 py-3)
- Secondary actions: Outlined or ghost variants
- Icon buttons for compact actions (size-10)

### Overlays
- Modal dialogs: Centered, max-w-2xl, with backdrop blur
- Side panels: Slide-in from right for case details (w-1/2)
- Notifications: Toast notifications top-right corner

## Page Structure

### Homepage/Landing
- Hero with impactful legal imagery + blurred-background CTAs
- Problem statement section (2-column: text + supporting visual)
- How it works (4-step process with icons)
- Success metrics (3-column grid)
- AI capabilities showcase (feature cards grid)
- Social proof (testimonials in 2-column)
- Final CTA section with contact form

### Dashboard
- Top metrics row (4 cards)
- Active cases table with filters
- Recent activity feed (side panel)
- Quick action buttons

### Case Detail Page
- Header with case number, status, dates
- 2-column layout: Main content (evidence, timeline, AI analysis) + Sidebar (actions, metadata, documents)
- Tabbed sections for organized information

## Icons
**Library**: Heroicons via CDN
- Consistent 24px size for UI elements
- 20px for inline text icons

## Animations
**Minimal approach**:
- Smooth transitions on hover states (transition-colors duration-200)
- Subtle loading spinners for async operations
- No scroll-triggered animations
- Page transitions: Simple fade (if using SPA)

## Images

**Hero Section**: 
- Large professional image showing scales of justice, courthouse columns, or abstract legal/justice symbolism
- Full-width background with overlay gradient for text readability
- Professional photography, not stock-looking

**Supporting Imagery**:
- Team section: Professional headshots if applicable
- Success stories: Before/after case resolution visuals (anonymized)
- Process diagrams: Custom illustrations for workflow steps

## Accessibility
- All form inputs with proper labels and aria-attributes
- Sufficient contrast ratios throughout
- Keyboard navigation for all interactive elements
- Screen reader friendly status updates
- Focus indicators on all focusable elements