# Book Bank
Mobile-first digital library web app built only on Cloudflare Workers, D1 and R2. No Supabase.

## Cloudflare resources
- Worker: book-bank-web
- D1 binding: DB -> book-bank-db
- R2 binding: FILES -> book-bank-pdfs
- Worker secret: ADMIN_PASSWORD

## Included
- Responsive bookshelf, collections and search
- Full-text page indexing for PDFs
- PDF.js page reader and page navigation
- Text-to-speech for the current page
- Bookmarks, notes and saved highlights
- Admin PDF upload and PDF indexing
- Light/dark reading theme and font controls

## First use
1. Set ADMIN_PASSWORD as a Worker secret.
2. Open Admin and sign in.
3. Choose "Index PDF library" and leave the tab open until it finishes.
4. New uploads should also be indexed after upload.

PDF text extraction uses PDF.js in the browser. Scanned/image-only PDFs require OCR before searchable text can be created. Notes and bookmarks currently use an anonymous browser-local user ID; add real login before public multi-user production use.

The Worker is deployed directly from Cloudflare. GitHub is the source repository.