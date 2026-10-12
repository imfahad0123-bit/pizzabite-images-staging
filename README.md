# pizzabite-images-staging

**STAGING ONLY.** Image assets for `pizza-bite-staging-api`
(`https://pizza-bite-staging-api.vercel.app`).

- Production images live in the **separate** repository `pizzabite-images`.
  Nothing in this repository is served to production, and the staging API's
  write credential is scoped to **this repository only**.
- Published by `POST /api/v1/admin/images` (staging API) into
  `assets/images/menu/<name>-<random8>.<ext>` (JPEG/PNG/WebP, max 2 MB).
- Browsers read files via
  `https://raw.githubusercontent.com/imfahad0123-bit/pizzabite-images-staging/main/<path>`
  (public repo so unauthenticated `<img>` requests work).
- `products.image_path` stores the relative path only (no `://`, no leading
  `/` — DB CHECK constraint).
