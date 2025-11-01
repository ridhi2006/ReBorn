# Ecovibe Design Guidelines

## Design Approach

**Reference-Based Approach** drawing inspiration from:
- **Airbnb**: Card-based marketplace layout, clean product showcases
- **Linear**: Modern dashboard aesthetics, crisp typography
- **Too Good To Go / Ecosia**: Eco-conscious visual language
- **Notion**: Organized information hierarchy and section layouts

**Core Principles:**
1. **Eco-conscious minimalism** - Clean, purposeful design that reflects sustainability values
2. **Friendly accessibility** - Welcoming interface that encourages engagement
3. **Visual storytelling** - Use imagery to inspire reuse and repair
4. **Gamified delight** - EcoPoints and rewards feel celebratory

---

## Typography System

**Font Families:**
- Primary: Inter or DM Sans (modern, clean sans-serif via Google Fonts)
- Accent: Space Grotesk for headings (slightly rounded, friendly character)

**Hierarchy:**
- **Hero/Page Titles**: 3xl to 6xl, bold weight
- **Section Headings**: 2xl to 3xl, semibold
- **Card Titles**: lg to xl, semibold
- **Body Text**: base (16px), regular weight
- **Labels/Metadata**: sm to base, medium weight
- **Captions**: sm, regular weight

---

## Layout System

**Spacing Primitives:** Use Tailwind units of **2, 4, 6, 8, 12, 16, 20, 24**
- Micro spacing: p-2, gap-4
- Component spacing: p-6, p-8
- Section spacing: py-12, py-16, py-20
- Page margins: px-4 (mobile), px-6 (tablet), px-8 (desktop)

**Grid System:**
- Max container width: max-w-7xl for full layouts
- Content max width: max-w-4xl for forms and focused content
- Dashboard: 12-column grid with responsive breakpoints
- Marketplace: 1 col (mobile) → 2 cols (tablet) → 3-4 cols (desktop)

**Responsive Breakpoints:**
- Mobile-first approach
- sm: 640px (tablets)
- md: 768px (small laptops)
- lg: 1024px (desktops)
- xl: 1280px (large screens)

---

## Component Library

### Navigation
**Primary Navbar:**
- Fixed top position with subtle shadow
- Logo left, nav links center, user profile/EcoPoints badge right
- Mobile: Hamburger menu with slide-in drawer
- Height: h-16 (64px)
- Links: Home, Chatbot, Repairer, Marketplace, Profile

**Footer:**
- Three-column layout (desktop), stacked (mobile)
- Column 1: Brand info and "Built with ❤️ by Ridhi"
- Column 2: Quick links (Terms, Privacy, About)
- Column 3: Social media icons
- Padding: py-12

### Authentication Pages
**Login/Signup:**
- Split screen layout: 50% hero image (left), 50% form (right) on desktop
- Centered card on mobile with image as background overlay
- Form card: max-w-md, rounded-2xl, shadow-xl
- Input fields: h-12, rounded-lg, border with focus ring
- CTA button: w-full, h-12, rounded-lg, font-semibold
- Social login option below primary form

### Dashboard
**Hero Section:**
- Personalized greeting: text-4xl to text-5xl, bold
- Subheading with user stats (items reused, EcoPoints earned)
- Primary CTA: "Upload Product Photo" - large button (h-14), rounded-full with icon
- Background: Soft gradient or hero image with product reuse examples

**EcoPoints Display:**
- Prominent card in top-right corner
- Large number display: text-3xl to text-4xl, bold
- Circular progress indicator or badge design
- Micro animation on points increase

**Upload Section:**
- Drag-and-drop zone: min-h-64, border-2 dashed, rounded-2xl
- Camera icon and "Click to upload or drag photo" text
- Preview thumbnail after upload
- Action buttons below: "Get AI Ideas" and "Contact Repairer"

**Quick Stats Cards:**
- Grid of 3-4 metric cards
- Each card: p-6, rounded-xl, shadow-md
- Icon + Number + Label structure
- Stats: Products Reused, CO2 Saved, Repairs Completed, EcoPoints

### AI Chatbot Interface
**Layout:**
- Full-width modal or dedicated page
- Chat messages: max-w-3xl centered
- Message bubbles: p-4, rounded-2xl, max-w-md
- User messages: align right
- AI messages: align left with avatar icon
- Input area: sticky bottom, h-16, rounded-full input with send button

**Message Types:**
- Text responses with rich formatting
- YouTube embed cards: rounded-xl, aspect-video, with title and "Watch Tutorial" link
- Repairer suggestion cards: compact profile with contact button
- Image analysis results with tagged suggestions

### Repairer Portal
**Repairer Dashboard:**
- Sidebar navigation (desktop) with metrics overview
- Main content area: pending requests, active jobs, completed work
- Request cards: p-6, rounded-xl, with product image, description, user contact
- Accept/Decline action buttons

**Repairer Profile Setup:**
- Multi-step form with progress indicator
- Skills tags with add/remove interaction
- Service area map integration placeholder
- Portfolio upload section: grid of uploaded work examples

### Marketplace
**Product Grid:**
- Masonry layout or equal-height cards
- Card structure: Image (aspect-square) + Title + Price + Repairer badge + CTA
- Hover effect: subtle scale and shadow increase
- Filter sidebar (desktop) or top bar (mobile): Categories, Price range, Condition

**Product Detail Modal/Page:**
- Large image gallery with thumbnails
- Right panel: Title, Price, Description, Repairer info, "Buy Now" button
- Tabs: Details, Sustainability Impact, Repairer Story

### Payment Integration
**Checkout Flow:**
- Two-column layout: Order summary (left), Payment form (right)
- Payment method selector: Cards for Google Pay, UPI, Stripe
- Form fields: card number, expiry, CVV with validation states
- Trust badges below payment form
- Confirmation screen with EcoPoints awarded message

### Buttons & CTAs
**Primary Actions:**
- Rounded-lg or rounded-full depending on context
- Height: h-12 for standard, h-14 for hero CTAs
- Font: semibold, text-base or text-lg
- Padding: px-8
- Icon + Text combination where relevant

**Secondary Actions:**
- Border style with transparent background
- Same dimensions as primary
- Hover state shows subtle fill

**Floating Action Buttons:**
- Fixed bottom-right for quick upload
- Rounded-full, w-14 h-14
- Icon only with tooltip on hover

### Cards
**Standard Content Card:**
- Rounded-xl, shadow-md, p-6
- Hover: shadow-lg transition
- Image (if present): rounded-t-xl, aspect-video or aspect-square

**Stat/Metric Card:**
- Rounded-xl, p-6, text-center
- Large icon or emoji at top
- Number: text-3xl, bold
- Label: text-sm

**Product/Marketplace Card:**
- Image: aspect-square, rounded-t-xl
- Content: p-4
- Badge for "Upcycled" or "Verified Repairer"
- Price: text-xl, bold
- CTA button at bottom

### Forms
**Input Fields:**
- Height: h-12
- Border radius: rounded-lg
- Border: border with focus:ring-2
- Padding: px-4
- Label: text-sm, font-medium, mb-2

**File Upload:**
- Drag-and-drop area: border-2 dashed, min-h-48, rounded-xl
- Icon and helper text centered
- Preview thumbnails in grid below

---

## Animations

**Use Sparingly:**
- Page transitions: Smooth fade-in (200-300ms)
- Card hover: Scale 1.02, shadow increase (200ms ease)
- EcoPoints increment: Number count-up animation
- Chat messages: Slide-in from bottom (300ms)
- Success states: Gentle bounce or checkmark animation

**NO animations for:**
- General scrolling
- Nav interactions
- Form inputs (except validation states)

---

## Images

### Hero Images:
1. **Landing Page Hero**: Large hero image (min-h-screen on desktop, 60vh on mobile) showing diverse products being creatively reused - furniture, electronics, clothing arranged artistically. Vibrant, optimistic composition.

2. **Dashboard Background**: Subtle background pattern or light image of nature/leaves, low opacity, adds texture without distraction.

3. **Authentication Pages**: Split-screen left side - inspirational image of beautiful upcycled products or community repair workshop scene.

### Section Images:
4. **Marketplace Product Photos**: Each product listing requires square images (aspect-square) showing the upcycled/repaired item clearly.

5. **Repairer Profiles**: Circular avatar images (aspect-square, rounded-full) for repairer identities.

6. **Tutorial Embeds**: YouTube video thumbnails embedded as cards within chatbot responses.

7. **Success/Empty States**: Illustration-style images for states like "No items yet" or "EcoPoints milestone reached" - friendly, eco-themed graphics.

---

## Key Page Layouts

### Landing/Dashboard Page (Authenticated):
- Full-width hero: Personalized greeting + Upload CTA + Hero image background
- Stats grid: 4 metric cards (grid-cols-1 md:grid-cols-2 lg:grid-cols-4)
- Recent activity feed: List of latest reuse actions
- EcoPoints progress card: Prominent, celebratory design
- Quick access buttons: Large icon buttons for Chatbot, Find Repairer, Browse Marketplace

### Chatbot Page:
- Clean, focused layout
- Product image pinned top-left (small thumbnail)
- Center-aligned chat interface (max-w-3xl)
- AI suggestions in rich cards with icons
- YouTube embeds in message stream
- Input bar sticky at bottom with attachment option

### Marketplace Page:
- Filter sidebar (desktop) or drawer (mobile)
- Main area: Product grid (grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4)
- Each card: Image + Title + Price + Repairer + "View Details"
- Pagination or infinite scroll at bottom

---

**Implementation Priority:** Create a visually rich, feature-complete experience from launch. Every section should feel polished and purposeful, celebrating sustainability through thoughtful design.