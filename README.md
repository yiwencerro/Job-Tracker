[README.md](https://github.com/user-attachments/files/30245044/README.md)
# Job Tracker — Supabase Version

This is a simple one-page job application tracker.

## Before opening the page

Open `index.html` in a text editor and find:

```javascript
const SUPABASE_URL = "PASTE_YOUR_SUPABASE_URL_HERE";
const SUPABASE_PUBLISHABLE_KEY = "PASTE_YOUR_PUBLISHABLE_KEY_HERE";
```

Replace both placeholders with the values from your Supabase project.

Use only the **Publishable / anon public key**. Never use the service-role key.

## Open the app

For a quick test, double-click `index.html`.

If your browser blocks authentication when opening a local file, run a local server:

### Windows

Open Command Prompt inside the folder and run:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Supabase requirements

Your `jobs` table should include:

- id
- created_at
- user_id
- url
- company
- job_title
- work_type
- company_salary_range
- expected_salary
- status
- applied_date
- notes

Row Level Security should be enabled, with authenticated users allowed to access only rows where `user_id = auth.uid()`.

## First use

1. Click **Create Account**.
2. Confirm your email if Supabase email confirmation is enabled.
3. Sign in.
4. Add your first job.
