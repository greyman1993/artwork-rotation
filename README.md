# Artwork Rotation (Supabase + GitHub Actions)

Automates rotating which artworks are visible in your Supabase database by calling the `rotate_artworks` RPC on a schedule (and on-demand).

- Live runs by default on schedule (`dry=false`)
- Manual runs with a `dry` toggle
- Sensible defaults for targets (via GitHub Secrets or hardcoded fallbacks)
- Clear run summaries and cURL retries
- No overlapping jobs (concurrency)

---

## How it works

A GitHub Actions workflow at `.github/workflows/rotate.yml` calls your Supabase RPC:

