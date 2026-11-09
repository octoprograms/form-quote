# form-quote

Pack-size confirmation form for Double Whiteline Plus Ltd (Kaizen Prompt Suppliers).

Static site — deploy on Vercel by importing this repo (no build step, framework preset "Other").
Access is protected by an access code, checked server-side in Supabase (`public.check_pack_form_code`, `public.submit_pack_confirmation`; hashed code in `kaizen_private.form_access_codes`, 20 wrong tries/hour lockout). The public key cannot read or insert into the table directly.
Answers land in `public.supplier_pack_confirmations` (project Course Finder).
