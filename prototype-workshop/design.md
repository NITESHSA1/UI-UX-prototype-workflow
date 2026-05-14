# Design Document: Interactive Prototype Creation Workshop

## 1. Profile Baseline Declaration

- **Profile selection**: `profiles/education.md` — Corporate Training variant
- **Selection rationale**: This is a skills-training workshop presentation teaching designers how to build interactive prototypes. The audience consists of UX/UI designers and product team members who need practical, actionable knowledge. The corporate training profile best matches the "practice-oriented, concise and clear" delivery style needed.
- **Referenced dimensions**: Information density (medium-high 65-80%), text-to-visual ratio (more text than images for tool explanations), font guidance (standard corporate training sizes), content expression techniques (numbered steps, comparison frameworks, checklists), decoration prohibitions
- **Deviation notes**: 
  - Visual sophistication elevated above standard corporate training — the audience is designers who appreciate refined aesthetics
  - Color palette deviates from typical corporate colors toward a design-tool-inspired dark/light contrast (Figma/Dark Mode aesthetic for special pages)
  - Layout uses more magazine-editorial and design-forward approaches than standard training templates

## 2. Style Baseline Declaration

- **Style anchor selection**: 
  - **Primary anchor: Figma's own design language** — Dark mode interface aesthetic, clean typography, purposeful whitespace, subtle rounded corners. This directly connects to the tool being taught.
  - **Secondary anchor: Apple's Keynote presentation style** — Dramatic cover slides with bold typography, clean content layouts, generous margins, and refined use of accent colors.
  - **Tertiary anchor: Swiss International Style** — Grid discipline, typographic hierarchy, clean alignment, rational information architecture.
- **Referenced dimension explanation**: 
  - From Figma: The dark-mode cover/chapter aesthetic, rounded element corners, color palette temperature, the sense of "design tool precision"
  - From Apple: Cover slide dramatic scale contrast, bold title treatments, generous breathing room
  - From Swiss Style: Grid alignment discipline, typographic scale hierarchy, information chunking

## 3. Style Details

### 3.1 Color Design Principles

**Overall color tendency**: In-between — stable foundation with local highlights. Cover/chapter pages use bold dark backgrounds; content pages use warm light backgrounds for readability.

**Temperature**: Warm-neutral. Charcoal blacks with warm amber/coral accents create a sophisticated, design-forward feel.

**Color decisions**:
- **Primary**: `#1A1A2E` — Deep warm charcoal (near-black with subtle navy warmth). Used for dark backgrounds on cover/chapter pages, and primary text on light pages. Avoids cheap blue-black.
- **Secondary**: `#6B7280` — Neutral warm gray. For body text, secondary information, annotations, borders.
- **Accent**: `#F97316` — Warm vibrant orange-amber. Energetic, creative, design-tool feel. Used sparingly for CTAs, key highlights, important data points.
- **Background (light)**: `#F9F8F6` — Warm off-white. Softer than pure white, creates a premium paper-like feel for content pages.
- **Background (dark)**: `#0F0F1A` — Deep warm black for cover/chapter/closing pages.
- **Light text**: `#F9F8F6` — For text on dark backgrounds.
- **Card fill**: `#F3F0EC` — Slightly darker warm tone for cards and containers on light pages.
- **Accent muted**: `#FFF7ED` — Very light orange tint for subtle highlight backgrounds.

### 3.2 Font Usage Principles

- **Title font**: `Liter` — Modern neo-grotesque, clean and rational. Perfect for a tech/design topic. Used with bold weight, all-caps for cover/chapter titles with expanded letter spacing.
- **Body font**: `QuattrocentoSans` — Classic elegant sans-serif, highly readable, gentle character. Excellent for education/training content at projection sizes.
- **Font size hierarchy**:
  - Cover title: 42px (Liter, all caps, letter-spacing 4px)
  - Cover subtitle: 20px (QuattrocentoSans)
  - Chapter title: 38px (Liter, all caps, letter-spacing 3px)
  - Page title: 28px (Liter, bold)
  - Body text: 20px (QuattrocentoSans, line-height 1.6)
  - Bullet points: 18px (QuattrocentoSans, line-height 1.5)
  - Annotations/labels: 14px (QuattrocentoSans)
  - Numbers/KPIs: 48-56px (Liter, bold, accent color)

### 3.3 Text Box and Container Styles

- **Content separation**: Primarily whitespace + font size hierarchy. Cards used selectively for grouping related content.
- **Card style**: Rounded rectangles (roundRect, adjustment 8000-12000), no border, filled with `#F3F0EC` or `#FFF7ED`. Subtle and warm.
- **Decorative elements**: 
  - Thin horizontal accent lines (2-3px, accent color) as section dividers
  - Small rounded accent-colored rectangles as bullet markers
  - Large semi-transparent chapter numbers as background decorative elements
  - Subtle corner accents on cover/chapter pages

### 3.4 Image Style

- **Icons**: Outline style (Font Awesome Regular), used moderately for key concepts. Accent color for icons on light pages; light color for icons on dark pages.
- **Tables**: Minimal style — accent-colored header row, alternating warm white/cream body rows, thin borders.
- **Charts**: Minimal flat style, monochrome with accent highlights, clean grid lines.
- **Illustrations**: High-quality photography showing design work environments, screens with prototypes, collaborative workshops. Dark, moody, professional aesthetic for cover/chapter pages.

## 4. Layout System

### 4.1 Global Layout Characteristics

- **Canvas**: 1280 x 720 (16:9)
- **Page margins**: 60px left/right, 50px top/bottom
- **Unified elements**:
  - Bottom-right: Small page category label (14px, secondary color) on content pages
  - Thin accent line (3px) at bottom of content pages as a grounding element
  - No navigation bar or sidebar — clean, uncluttered
- **Grid alignment**: All content aligned to an invisible 12-column grid. Elements snap to consistent left margins and widths.

### 4.2 Special Page Layouts

- **Cover page**: Hero design — full-bleed dark background image with gradient mask overlay. Large centered title in all-caps with wide letter spacing. Subtitle below in lighter weight. Small accent line between title and subtitle.
- **Table of Contents**: Asymmetric two-column — left side features large "AGENDA" heading vertically or at angle; right side shows three chapter cards with numbers and descriptions. Grid layout with equal-width chapter blocks.
- **Chapter transition pages**: Hero design — full-bleed image with dark gradient mask. Large semi-transparent chapter number (120px+) as watermark. Chapter title centered in all-caps. Brief subtitle below.
- **Final page**: Similar to cover — dark background, centered key takeaway message, closing statement.

### 4.3 Content Page Layout Patterns

- **Pattern A: Title + Two-column content** — Page title at top, content split into two equal columns below. Good for comparisons or parallel concepts.
- **Pattern B: Title + Left text + Right visual** — Title at top, explanatory text on left (60%), supporting diagram/visual on right (40%).
- **Pattern C: Title + Full-width structured content** — Title at top, content organized as numbered steps, cards in a row, or a structured list spanning full width.
- **Pattern D: Title + Grid cards** — Title at top, 2-3 cards arranged horizontally with icons and descriptions.
- **Pattern E: Title + Top illustration + Bottom text** — For process flows or diagrams at top with explanatory text below.

## 5. Style Usage Rules

### textStyle usage:
- `title`: Cover title, chapter titles — large, bold, all-caps treatment
- `heading`: Page titles on content pages — bold, primary color
- `body`: Main body text — readable size, comfortable line height
- `caption`: Annotations, labels, source text — smaller, secondary color
- `accent_number`: Large KPI numbers, step numbers — large, accent color, bold
- `label`: Category tags, small badges — small, may have background

### Color allocation:
- `$primary` (#1A1A2E): Dark backgrounds, primary text on light pages, strong emphasis
- `$secondary` (#6B7280): Body text on light pages, captions, secondary info
- `$accent` (#F97316): Key highlights, CTAs, important numbers, bullet markers, accent lines
- `$background` (#F9F8F6): Light page backgrounds
- `$dark` (#0F0F1A): Cover/chapter dark backgrounds
- `$light` (#F9F8F6): Text on dark backgrounds
- `$cardFill` (#F3F0EC): Card/container fills on light pages
- `$muted` (#FFF7ED): Subtle highlight backgrounds

### tableStyle usage:
- `default`: Standard data tables — accent header, alternating body rows

## 6. Risk Prohibitions

- [ ] **No cheap blue/cyan**: Stick to the warm charcoal + orange palette. No default blue accents.
- [ ] **No gradient abuse**: Gradients only for image masks on cover/chapter pages. No decorative gradients.
- [ ] **No dense text walls**: Maximum 6 bullet points per section; use cards or columns to break up content
- [ ] **No purely decorative images**: Every image must relate to prototyping/design/UX content
- [ ] **No misaligned layouts**: Left-right layouts must have aligned bottoms; grids must be perfectly even
- [ ] **No font size below 14px**: Annotations minimum 14px; body minimum 18px; titles minimum 28px
- [ ] **No large dark content pages**: Dark backgrounds reserved for cover/chapter/final only
- [ ] **No cliche icons**: Avoid overused metaphors; choose purposeful icons
- [ ] **No centered body text**: Body text always left-aligned; only titles and special callouts may be centered
- [ ] **No excessive card usage**: Prefer whitespace separation; cards only for clear content grouping

## 7. Theme Definition

```yaml
theme:
  colors:
    primary: "#1A1A2E"
    secondary: "#6B7280"
    accent: "#F97316"
    background: "#F9F8F6"
    dark: "#0F0F1A"
    light: "#F9F8F6"
    cardFill: "#F3F0EC"
    muted: "#FFF7ED"
  textStyles:
    title:
      fontSize: 42
      color: "$light"
      fontFamily: "Liter"
      letterSpacing: 4
      lineHeight: 1.2
    heading:
      fontSize: 28
      color: "$primary"
      fontFamily: "Liter"
      lineHeight: 1.3
    body:
      fontSize: 20
      color: "$secondary"
      fontFamily: "QuattrocentoSans"
      lineHeight: 1.6
    caption:
      fontSize: 14
      color: "$secondary"
      fontFamily: "QuattrocentoSans"
      lineHeight: 1.4
    accent_number:
      fontSize: 48
      color: "$accent"
      fontFamily: "Liter"
      lineHeight: 1.1
    label:
      fontSize: 14
      color: "$secondary"
      fontFamily: "QuattrocentoSans"
      lineHeight: 1.4
      backgroundColor: "$muted"
  tableStyles:
    default:
      fontSize: 16
      fontFamily: "QuattrocentoSans"
      headerFill: "$primary"
      headerColor: "$light"
      headerBold: true
      bodyFill: ["$background", "$cardFill"]
      bodyColor: "$primary"
      border:
        style: solid
        width: 1
        color: "#E5E2DE"
```
