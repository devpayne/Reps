# repstraining.com

The website for Reps, hosted on **GitHub Pages**. This repo holds the site's
pages, and GitHub publishes them automatically whenever a change is pushed —
no more dragging files into Netlify Drop.

## The pages

Each page lives in its own folder as `index.html`, which is what gives the
site clean URLs (`/pricing` instead of `/pricing.html`).

| URL                | File                            | What it is             |
|--------------------|---------------------------------|------------------------|
| `/`                | `index.html`                    | Homepage               |
| `/pricing`         | `pricing/index.html`            | Pricing page           |
| `/trainers`        | `trainers/index.html`           | Trainers page          |
| `/players-parents` | `players-parents/index.html`    | Players & parents page |
| `/combine-signup`  | `combine-signup/index.html`     | Combine signup page    |
| `/support`         | `support/index.html`            | Support page           |
| `/privacy`         | `privacy/index.html`            | Privacy policy         |
| `/terms`           | `terms/index.html`              | Terms of service       |

Shared images and videos live in `assets/` and are referenced with absolute
paths (`/assets/...`). The rest of each page's styling and images are built
into the file itself.

The combine signup form submits to an external Supabase checkout endpoint, so
it works the same no matter where the site is hosted.

## How to publish a change (plain English)

1. A change gets made to one of the pages above (Claude Code can do this for you).
2. The change is **committed** — a saved snapshot with a short note describing it.
3. The commit is **pushed** to GitHub.
4. GitHub Pages sees the push and **automatically publishes** the update,
   usually within a minute. No dragging files, no manual uploads.

To undo anything, an earlier snapshot can always be restored — nothing is
ever truly lost.

## Hosting setup (one-time)

- **Source:** GitHub Pages is set to deploy from the default branch, root folder.
- **Custom domain:** the `CNAME` file pins `repstraining.com`. The domain's DNS
  must point at GitHub Pages for the custom domain to go live.
- **`.nojekyll`** tells GitHub to serve the files exactly as-is (no Jekyll build).
