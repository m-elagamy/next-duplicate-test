# Next.js `'next/cache'` Duplication Bug

This minimal Next.js project demonstrates duplicate imports for all exports from `'next/cache'`, after building, (e.g., `revalidatePath`, `revalidateTag`) and an abnormal build size increase.

## Steps to Reproduce

1. Clone: `git clone https://github.com/m-elagamy/nextjs-cache-duplication.git`
2. Install: `npm install`
3. Build: `npm run build`
4. Check:
   - Duplicate imports from `'next/cache'` (e.g., `revalidatePath`, `revalidateTag` in IDE autocomplete).
   - Size before/after build.

## Observed Behavior

- Fresh size: 351MB
- Post-build size: 398MB
- Duplicates: All exports from `'next/cache'` (e.g., `revalidatePath`, `revalidateTag`) appear duplicated.

## Expected Behavior

- Single import for each export from `'next/cache'`.
