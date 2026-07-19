# Anthony Hinojosa, Career Site

Live site: https://anthonyhinojosa77.github.io

Static personal career website for Anthony Hinojosa: industrial laboratory
technician, NREMT, FAA Part 107 remote pilot, and computer science student,
covering quality, safety, and operations work across Gulf Coast refineries
and labs.

Built with plain HTML5, CSS3, and vanilla JavaScript (ES6+). No frameworks,
no dependencies, no build step. The only external dependency is Google Fonts
(Instrument Serif, Inter, JetBrains Mono). The contact form delivers through
FormSubmit.

## Design system

The visual system is "Industrial Precision": a paper/ink palette with a single
signal-orange accent (#C2441C), editorial serif display type, and mono
technical readouts. Design tokens live in `css/system.css`; the full system
and the house rules (including the no-em-dash rule) are documented in
`CLAUDE.md`. Read it before changing markup, styles, or conventions.

## Run locally

No build step. Serve the folder with any static file server:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly in a browser also works.

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero, ticker, stats, capability index, featured work |
| About | `about.html` | Narrative, headshot, leadership philosophy |
| Experience | `experience.html` | Capability cards, timeline, work history |
| Map | `mindmap.html` | Interactive experience map with expand/collapse + camera pan |
| STAR Story | `star.html` | STAR story template, one per domain via `?domain=` |
| Projects | `projects.html` | STAR-format case studies with category filter |
| Certifications | `certifications.html` | Active certs + in-progress education |
| Skills | `skills.html` | Six skill domains, each linking to its STAR story |
| Writing | `blog.html` | Writing listing with category filter |
| Blog Post | `blog-post.html` | Full article (AI + QA in refineries) |
| Resume | `resume.html` | Web resume + PDF download, print-friendly |
| Contact | `contact.html` | Contact form + info |
| Not Found | `404.html` | Styled 404 page (noindex) |

## Structure

```
career-site/
├── index.html
├── about.html
├── experience.html
├── mindmap.html
├── star.html
├── projects.html
├── certifications.html
├── skills.html
├── blog.html
├── blog-post.html
├── resume.html
├── contact.html
├── 404.html
├── css/
│   ├── system.css      # Design tokens, reset, shared components
│   └── pages.css       # Tweaks panel + page-specific styles
├── js/
│   ├── site.js         # Reveal, counters, theme/tweaks, filters, clock
│   ├── mindmap-data.js # Experience-map data
│   └── mindmap.js      # Experience-map engine
├── images/
│   ├── favicon.ico
│   └── headshot.jpg
├── resume.pdf
├── sitemap.xml
├── robots.txt
├── README.md
└── CLAUDE.md
```

## Deployment

Hosted on GitHub Pages as a user-root site. Push this repo to `main` of
`AnthonyHinojosa77/AnthonyHinojosa77.github.io` and Pages serves the repo
root as-is: `sitemap.xml` and `robots.txt` at the root, `404.html` as the
not-found page. Do not add a `CNAME` file unless a custom domain is
configured; it would redirect the github.io URL.
