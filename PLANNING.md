# Project Planning - Fördermittel-Beratung Website

## Project Overview

**Client**: Government Funding Consulting Business
**Project Type**: B2B Consulting Website with Appointment Booking
**Target Audience**: German businesses seeking government funding (Fördermittel)
**Primary Goal**: Convert visitors into booked consultations

## Architecture & Technology Decisions

### Tech Stack
- **Framework**: Next.js 14 (App Router) with TypeScript
- **Styling**: Tailwind CSS + shadcn/ui components
- **Animations**: Framer Motion
- **Icons**: Lucide React
- **Booking**: Cal.com (open-source) or Calendly
- **Deployment**: Vercel (primary) or Netlify (alternative)
- **Analytics**: Google Analytics 4
- **Forms**: React Hook Form + Zod validation

### Project Structure
```
foerdermittel-consulting-website/
├── src/
│   ├── app/                    # Next.js app router pages
│   │   ├── page.tsx           # Homepage
│   │   ├── services/          # Service pages
│   │   ├── about/             # About page
│   │   └── contact/           # Contact page
│   ├── components/            # React components
│   │   ├── ui/               # shadcn/ui components
│   │   ├── sections/         # Page sections
│   │   └── booking/          # Booking widgets
│   ├── lib/                  # Utilities
│   └── styles/               # Global styles
├── public/                   # Static assets
├── content/                  # MDX content files
└── tests/                    # Pytest tests (if backend needed)
```

## Design Principles

### Visual Design
- **Professional & Trustworthy**: Corporate blue/green color scheme
- **Clean & Modern**: Ample white space, clear typography
- **Conversion-Focused**: Strategic CTA placement
- **Mobile-First**: Responsive design for all devices

### UX Principles
- **Clarity**: Clear value proposition within 3 seconds
- **Simplicity**: Max 2 clicks to any important page
- **Trust**: Social proof and credentials prominently displayed
- **Speed**: Fast page loads (<2s)

### Conversion Strategy
- **Above-the-fold CTAs**: Every page
- **Multiple booking entry points**: Service pages, sticky buttons
- **Progressive disclosure**: Don't overwhelm visitors
- **Reduced friction**: Minimal form fields, one-click booking

## Content Strategy

### Page Hierarchy
1. **Homepage** (Priority: Highest)
   - Hero with value proposition
   - Services overview
   - Why choose us
   - Process overview
   - Social proof
   - Final CTA

2. **Service Pages** (Priority: High)
   - Individual pages for each service
   - Problem/solution framework
   - Benefits & value
   - Process steps
   - Pricing
   - Booking widget

3. **About/Expertise** (Priority: Medium)
   - Company story
   - Team expertise
   - Industry focus

4. **Contact** (Priority: Medium)
   - Contact form
   - Booking calendar
   - Office information

### Tone & Voice
- **Professional but approachable**
- **Benefit-focused** (not feature-focused)
- **Clear and concise** (B2B audience values time)
- **Action-oriented** (guide to next steps)

## Competitive Positioning

### Key Differentiators vs. Leyton Deutschland
- Modern, faster website technology
- Cleaner, more focused user experience
- Integrated booking (not separate contact form)
- Better mobile experience

### Key Differentiators vs. Innoscripta
- More personalized consulting approach (vs. SaaS platform)
- Simpler, clearer service offerings
- Faster booking process
- More accessible pricing

## Development Phases

### Phase 1: Foundation
- Project setup (Next.js, TypeScript, Tailwind)
- Component library setup (shadcn/ui)
- Design system (colors, typography, spacing)
- Base layout (header, footer, navigation)

### Phase 2: Core Pages
- Homepage development
- Service page template
- Individual service pages (3-5)
- About page
- Contact page

### Phase 3: Booking Integration
- Cal.com/Calendly setup
- Booking widget components
- Email automation
- Payment integration (if needed)

### Phase 4: Optimization
- SEO optimization
- Performance optimization
- Analytics setup
- Cross-browser testing
- Mobile testing

### Phase 5: Launch
- Domain setup
- SSL configuration
- Production deployment
- Documentation
- Training

## File Naming Conventions

### Components
- PascalCase: `BookingWidget.tsx`, `ServiceCard.tsx`
- Collocate tests: `BookingWidget.test.tsx`

### Pages
- kebab-case: `forschungszulage-beratung/page.tsx`

### Utilities
- camelCase: `formatDate.ts`, `validateEmail.ts`

### Content
- kebab-case: `forschungszulage-beratung.mdx`

## Code Style Guidelines

### TypeScript
- Use strict mode
- Explicit return types for functions
- Interface over type (for objects)
- Avoid `any` type

### React
- Functional components only
- Custom hooks for reusable logic
- Props interfaces defined inline or exported
- Use React Server Components where possible (Next.js 14)

### Styling
- Tailwind utility classes (primary)
- CSS modules for complex components (if needed)
- Consistent spacing scale (4px base)
- Mobile-first responsive design

### Testing
- Unit tests for utilities
- Integration tests for booking flow
- E2E tests for critical paths (optional)

## SEO Strategy

### Technical SEO
- Semantic HTML structure
- Meta tags (title, description, OG tags)
- Schema.org markup (Organization, Service, FAQPage)
- Sitemap.xml
- Robots.txt
- Fast Core Web Vitals

### Content SEO
- Target keywords: "Fördermittelberatung", "Forschungszulage", etc.
- Long-tail keywords in service pages
- Internal linking strategy
- Alt text for all images

## Analytics & Tracking

### Key Metrics
- **Traffic**: Page views, unique visitors, traffic sources
- **Engagement**: Time on page, bounce rate, pages per session
- **Conversions**: Booking completions, form submissions
- **Funnel**: Homepage → Service page → Booking

### Events to Track
- CTA clicks
- Booking widget interactions
- Form submissions
- Phone number clicks
- Email clicks
- Download clicks (if resources offered)

## Maintenance & Updates

### Content Updates
- Client can update via MDX files
- No coding required for text changes
- Image updates via public folder

### Technical Updates
- Monthly dependency updates
- Security patches as needed
- Performance monitoring
- Analytics review

## Risk Mitigation

### Technical Risks
- **Browser compatibility**: Test on all major browsers
- **Mobile performance**: Optimize images, lazy loading
- **Booking integration**: Thorough testing of calendar sync

### Business Risks
- **Content delays**: Provide placeholder content
- **Scope creep**: Clear deliverables in contract
- **Payment integration**: Test thoroughly before launch

## Success Criteria

### Launch Criteria
- ✅ All pages responsive (mobile, tablet, desktop)
- ✅ Booking system functional and tested
- ✅ SEO basics implemented
- ✅ Analytics tracking active
- ✅ Performance: Lighthouse score >90
- ✅ Accessibility: WCAG 2.1 AA compliant
- ✅ Cross-browser tested (Chrome, Firefox, Safari, Edge)

### Post-Launch Goals (3 months)
- 1,000+ monthly visitors
- 5%+ conversion rate (visitors to bookings)
- <2s average page load time
- Top 10 ranking for target keywords

## Notes

- Client has existing logo (to be integrated)
- German language for all UX content
- GDPR compliance required
- Focus on B2B audience (not B2C)
