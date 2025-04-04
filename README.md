# Next.js `'next/cache'` Duplication Bug

This minimal Next.js project demonstrates duplicate imports for all exports from `'next/cache'`, after building, (e.g., `revalidatePath`, `revalidateTag`) and an abnormal build size increase.

## Steps to Reproduce

1. Clone: `git clone https://github.com/m-elagamy/next-duplicate-test.git`
2. Install: `npm install`
3. Build: `npm run build`
4. Check:
   - Duplicate imports from `'next/cache'` (e.g., `revalidatePath`, `revalidateTag` in IDE autocomplete).
   - Size before/after build (e.g., `.next` folder).

## Observed Behavior

- Fresh size: [Your fresh size, e.g., 351MB]
- Post-build size: [Your post-build size, e.g., 398MB]
- `.next` size: [Your .next size, e.g., 47MB]
- Duplicates: All exports from `'next/cache'` (e.g., `revalidatePath`, `revalidateTag`) appear duplicated.

## Expected Behavior

- Single import for each export from `'next/cache'`.
- Minimal size increase (e.g., `.next` ~10-20MB).
