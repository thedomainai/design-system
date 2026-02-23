# theDomainAI Design System

A multi-theme design system for theDomainAI brand, covering digital, paper, and utopia aesthetics.

## Themes

| Theme | Description | Primary Use Cases |
|-------|-------------|-------------------|
| **concept-master** | Canonical definition source with placeholders | Template for creating new themes |
| **digital** | Dark glass aesthetic with modern UI elements | Web apps, mobile apps, digital presentations |
| **paper** | Editorial magazine-inspired grayscale design | Documents, reports, white papers |
| **utopia** | Luxury aesthetic with gold accents and glaze effects | Premium presentations, brand materials |

## Directory Structure

Each theme follows a unified structure:

```
{theme}/
  design-system.md       ← Single Source of Truth (SSOT)
                           Defines Foundations, Materials, Components,
                           Patterns, and Platform Guidelines

  viewers/               ← Visual preview tools (open in browser)
    master.html          ← Complete design system viewer (required)
    color-palette.html   ← Color palette gallery (digital, utopia)
    presentation.html    ← Presentation viewer (digital, utopia)
    ui.html              ← Web UI viewer (digital only)

  templates/             ← Generation templates for AI content creation
    presentation.html    ← Presentation skeleton (digital, utopia)
    ui.html              ← Web UI component skeleton (digital only)
    thumbnail.html       ← OGP/YouTube thumbnail skeleton (digital only)

  references/            ← Reference materials & experimental code (optional)
    inspiration.md       ← Reference URL list
    *.html, *.css        ← Experimental code snippets
```

### Directory Roles

| Directory | Role | Description |
|-----------|------|-------------|
| `design-system.md` | Single Source of Truth | AI references this file when generating content |
| `viewers/` | Visual preview | View design-system.md definitions in browser (read-only) |
| `templates/` | Generation skeleton | HTML templates AI uses to generate media-specific content |
| `references/` | Inspiration & experiments | Design inspiration, CSS snippets, experimental HTML (optional) |

## Theme Characteristics

| Theme | Lines | Section Format | Colors | Fonts |
|-------|-------|----------------|--------|-------|
| **digital** | 1,712 | Numbered (## 1. ~ ## 13.) | Dark (#000000) + Glass | DM Sans + JetBrains Mono |
| **paper** | ~835 | Numbered (## 1. ~ ## 15.) | Grayscale only (#fdfdfc) | Crimson Pro + Instrument Sans + JetBrains Mono |
| **utopia** | 1,596 | Numbered (## 1. ~ ## 14.) | Dark (#0c0a08) + Gold | Playfair Display + Source Sans 3 + JetBrains Mono |

## Usage

### Viewing Design Systems

Open `{theme}/viewers/master.html` in your browser to preview the complete design system visually.

### Generating Content

AI agents reference `{theme}/design-system.md` as the SSOT and use templates in `{theme}/templates/` to generate:
- Presentations (pptx/HTML)
- Web UI components
- Mobile app screens
- Thumbnails (OGP, YouTube)

### Adding New Platforms

To add a new platform (e.g., "email"):
1. Add platform guidelines to the "Platform Guidelines" section in `design-system.md`
2. (Optional) Create `templates/email.html` if AI-generated templates are needed
3. (Optional) Create `viewers/email.html` for visual preview

## Platform Coverage

All themes include guidelines for:
- **Web Page** — Marketing sites, landing pages
- **Web App** — Dashboard, SaaS applications
- **Mobile App (iOS)** — Native iOS apps following HIG
- **Visual Presentation** — PowerPoint/Keynote slides

## Development

### Structure Consistency

All three themes (digital, paper, utopia) maintain structural consistency:
- Numbered section headings (## 1. ~ ## N.)
- Reference paths use section numbers (e.g., "Section 2 (Color System)")
- `viewers/master.html` is required for all themes
- Other viewers and templates are added incrementally based on theme needs

### Mobile App (iOS) Guidelines

The Mobile App section (~100 lines) covers iOS HIG essentials:
- Layout & Touch Targets (44pt minimum)
- Navigation Patterns (Tab Bar, Navigation Bar, Modal/Sheet)
- Interaction & Feedback (Response Time, Haptics, Loading)
- Typography Mapping (SF Pro fonts, Dynamic Type)
- Component Mapping
- Motion & Animation

### Presentation Guidelines

All themes share a unified Presentation structure:
- Typography: weights are +1 step heavier than web
- Minimum font sizes:
  - digital/utopia: 10px (copyright only)
  - paper: 14pt (all text including copyright)

## License

Proprietary — theDomainAI internal use only.
