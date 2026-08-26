# Andie Tech Solutions — Technical Documentation

## 1. Current public site (Version 2)

**Live URL:** `https://egoria-andrew.github.io/andie-tech-solutions/`

The site is a static marketing website for Andie Tech Solutions. It is hosted on GitHub Pages and is designed to convert visitors into WhatsApp enquiries.

### Technology

| Area | Current implementation |
| --- | --- |
| Structure | HTML5 |
| Styling | CSS3 with responsive breakpoints |
| Icons | Font Awesome CDN |
| Hosting | GitHub Pages |
| Enquiries | Pre-filled WhatsApp links |
| Dynamic data | None |

### Main pages

| File | Purpose |
| --- | --- |
| `index.html` | Home page: services, tech tip, and contact call-to-action |
| `fixes.html` | Quick Fixes page with basic self-help steps |
| `index2.html` | Compatibility redirect for the former Quick Fixes URL |
| `style.css` | Shared responsive styling |

### Brand assets

| Asset | Purpose |
| --- | --- |
| `assets/andie-tech-wordmark.png` | Header and footer logo |
| `assets/andie-tech-hero.png` | Hero illustration |
| `assets/favicon.png` | Browser favicon |

### Responsive behaviour

- Desktop: three-column service grid and horizontal navigation.
- Tablet: service grid changes to two columns.
- Phone: navigation becomes a hamburger menu; service cards, footer content, contact panel, and hero content stack vertically.

### Version 2 maintenance note

The live services grid includes web and digital solutions, laptop repair and upgrades, and network support. Keep the footer’s **What we offer** list updated with the same service categories whenever the services section changes.

## 2. Future internal service dashboard

The dashboard should be a separate future feature, not a replacement for the public customer website. The public site should continue to focus on services and WhatsApp booking. The dashboard should help you organise work that arrives through WhatsApp.

### Dashboard goals

- Record new customer enquiries.
- Track laptop jobs, website jobs, and network jobs.
- See active, completed, and pending work at a glance.
- Keep customer contact details, job notes, price estimates, and status in one place.
- Create a clear history of completed work and payments.

### Suggested screens

| Screen | Main content |
| --- | --- |
| Dashboard home | Summary cards, recent enquiries, active jobs, quick actions |
| Service leads | New WhatsApp enquiries and their follow-up status |
| Repairs & upgrades | Device, issue, diagnosis, parts, estimate, and status |
| Website projects | Client, project type, package, deadline, progress, and URL |
| Network jobs | Client, location, issue, quote, and completion status |
| Customers | Customer contact details and job history |
| Quick Fixes manager | Draft and publish future tech tips |

### Suggested job statuses

`New` → `Contacted` → `Quoted` → `In progress` → `Awaiting customer` → `Complete` → `Cancelled`

Use the same status names everywhere so dashboard totals remain meaningful.

## 3. Build approach

### Phase A — HTML and CSS prototype

Build the dashboard layout with only HTML and CSS first.

- Branded sidebar and top bar.
- Responsive cards and tables.
- Example customer records and job statuses.
- Mobile layout that stacks content and turns the sidebar into a menu.

This is the right first step because it establishes the structure and visual design quickly.

**Important:** an HTML/CSS dashboard is only a visual prototype. It does not have real login protection, saved data, or working filters. Do not store customer data in it yet.

### Phase B — working dashboard

After the interface is approved, add:

- JavaScript for forms, filters, totals, and status updates.
- Authentication so only you can access the dashboard.
- A database for customers, jobs, notes, and payment data.

A practical low-maintenance option is a hosted backend such as Firebase or Supabase. GitHub Pages can continue to host the static dashboard interface, but secure login and data must come from a backend service.

### Suggested folder structure

```text
andie-tech-solutions/
├── index.html                 # Public website
├── fixes.html                 # Public Quick Fixes page
├── assets/
├── style.css
└── dashboard/
    ├── index.html             # Dashboard home
    ├── leads.html
    ├── repairs.html
    ├── web-projects.html
    ├── dashboard.css
    └── dashboard.js           # Added in Phase B
```

Do not link the dashboard from the public main navigation until authentication is implemented.

## 4. Website address options

The current address is a **GitHub Pages project site**. GitHub project sites use this pattern:

```text
https://<GitHub-username>.github.io/<repository-name>/
```

That is why the live URL includes `egoria-andrew.github.io/` before `andie-tech-solutions`.

### Option A — Keep the current free URL

`https://egoria-andrew.github.io/andie-tech-solutions/`

Free and reliable, but longer.

### Option B — Use `egoria-andrew.github.io` as the site root

Rename/create the user-site repository as `egoria-andrew.github.io`. The URL becomes:

`https://egoria-andrew.github.io/`

This removes `/andie-tech-solutions/`, but the GitHub username remains. It is useful if this will be your only main site.

### Option C — Recommended: buy a custom domain

Examples: `andietechsolutions.com`, `andietech.ug`, or `andietechsolutions.ug`.

Then the address can be simply:

`https://andietechsolutions.com/`

This is the only option that removes the GitHub username and gives the business a fully branded web address. GitHub Pages supports custom domains and HTTPS once the domain’s DNS records are connected. See GitHub’s [custom-domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## 5. Recommended next step

Keep Version 1 preserved in Git history and maintain the current public site as Version 2. When ready, create the dashboard as a separate `dashboard/` prototype, approve its HTML/CSS design, then connect secure authentication and data storage.
