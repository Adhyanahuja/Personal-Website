# What to change when personalizing

Everything visitors see is either in **`index.html`** or in **images** under `assets/images/`. JS and CSS contain no personal data.

---

## 1. `index.html` — all text and links

### Head (top of file)
| What | Where | Change to |
|------|--------|-----------|
| Page title (browser tab) | `<title>` (~line 8) | Your name / site title |
| Favicon | `href="./assets/images/logo.ico"` (~line 13) | Optional: point to your favicon file |

---

### Sidebar (~lines 39–150)
| What | Change to |
|------|-----------|
| Avatar image | `./assets/images/my-avatar.png` — replace the file or path |
| Avatar `alt` text | Your name |
| `<h1 class="name">` and `title` | Your full name |
| `<p class="title">` | Your job title (e.g. "Web developer", "Designer") |
| Email | `mailto:` link and visible address |
| Phone | `tel:` link and visible number |
| Birthday | `<time datetime="YYYY-MM-DD">` and display text |
| Location | `<address>` text |
| Social links (Facebook, Twitter, Instagram) | `href="#"` → your profile URLs |

---

### About (~lines 204–510)
| What | Change to |
|------|-----------|
| "About me" paragraphs | Your bio (two `<p>` blocks in `section.about-text`) |
| "What i'm doing" | Up to 4 service items: icon, title (e.g. "Web design"), and short description |
| Testimonials (optional) | 4 cards: avatar image, name, quote, and modal date; or remove the testimonials block |
| Testimonial text | Still says "Richard" in quote text — replace with your name or real quotes |

---

### Resume (~lines 515–702)
| What | Change to |
|------|-----------|
| Education | Each `li.timeline-item`: school name (`h4`), date range (`span`), description (`p.timeline-text`) |
| Experience | Same structure: role, dates, description |
| My skills | Each `li.skills-item`: skill name (`h5`), percentage (`data` and `style="width: ..."`) |
| Add/remove | Duplicate or delete `<li class="timeline-item">` / `<li class="skills-item">` blocks as needed |

---

### Portfolio (~lines 708–938)
| What | Change to |
|------|-----------|
| Filter buttons | "All", "Web design", "Applications", "Web development" — change labels and keep filter text in sync with `data-category` |
| Project cards | Each `li.project-item`: `data-category` (lowercase), `href` (project URL), image `src`/`alt`, `h3.project-title`, `p.project-category` |
| Categories | Must match between filter buttons, `data-select-item` buttons, and each card’s `data-category` |
| Images | `./assets/images/project-1.jpg` … `project-9.png` — replace with your project thumbnails or remove cards |

---

### Blog (~lines 948–1128)
| What | Change to |
|------|-----------|
| Each post | Image `src`/`alt`, `blog-category`, `<time>`, `blog-item-title`, `blog-text`, and link `href` |
| Images | `./assets/images/blog-1.jpg` … `blog-6.jpg` — replace or remove posts |
| Optional | Remove the whole Blog section or hide it via nav/CSS if you don’t use it |

---

### Contact (~lines 1140–1176)
| What | Change to |
|------|-----------|
| Map iframe | `src` of the `<iframe>` — replace with your own Google Maps embed URL (or remove map) |
| Contact form | `form action="#"` — form doesn’t submit anywhere by default; hook up a backend, Formspree, or similar and set `action` (and optionally `method`) |

---

## 2. `assets/images/` — images to replace

| File | Used for |
|------|----------|
| **my-avatar.png** | Your photo in the sidebar (and possibly elsewhere). Replace with your own image. |
| **logo.ico** | Favicon (browser tab icon). Replace for a custom favicon. |
| **avatar-1.png** … **avatar-4.png** | Testimonial avatars (About section). Replace if you keep testimonials. |
| **project-1.jpg** … **project-9.png** | Portfolio project thumbnails. Replace with your project images or remove cards. |
| **blog-1.jpg** … **blog-6.jpg** | Blog post banners. Replace with your images or remove posts. |

Icons (e.g. `icon-design.svg`, `icon-dev.svg`, `logo.svg`) are generic; change only if you want different icons.

---

## 3. Files you don’t need to edit for content

| File | Contains |
|------|----------|
| **assets/js/script.js** | Sidebar toggle, testimonial modal, portfolio filter, form validation, page navigation. No names, links, or copy. |
| **assets/css/style.css** | Layout and styling only. No personal data. |

---

## Quick checklist

- [ ] `index.html`: title, sidebar (name, title, email, phone, birthday, location, social links)
- [ ] `index.html`: About (bio, services, testimonials)
- [ ] `index.html`: Resume (education, experience, skills)
- [ ] `index.html`: Portfolio (filters, project cards, categories)
- [ ] `index.html`: Blog (posts or remove)
- [ ] `index.html`: Contact (map embed, form `action`)
- [ ] `assets/images/`: my-avatar.png, logo.ico
- [ ] `assets/images/`: portfolio and blog images (if you use those sections)
