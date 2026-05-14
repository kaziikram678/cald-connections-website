# CLAD Website Handoff

## Overview

This project is a static single-page website for CALD Connections / CLAD Website content.
It is currently deployed on Vercel and served from `index.html`.

Production URL:

- `https://clad-website.vercel.app/`

## Current File Structure

- `index.html` - main live website file
- `images/` - local image assets used by the website
- `vercel.json` - Vercel config
- `.vercel/` - local Vercel project link metadata
- `.gitignore` - includes `.vercel`

## Current Working Folders

There are currently two local copies on the Desktop:

- `C:\Users\User\Desktop\CLAD Website`
- `C:\Users\User\Desktop\CLAD Website_2026-05-04`

Important:

- The latest Vercel production deploy was pushed from `CLAD Website_2026-05-04`
- VS Code may still be opened on `CLAD Website`
- Recent edits were synced between the two so production is up to date

Recommended cleanup:

- Close the old folder in VS Code / File Explorer
- Continue working from `CLAD Website_2026-05-04`
- Remove the old `CLAD Website` folder once it is no longer locked

## Important Note

`index.html` is the live source file.

There used to be a `main.html` workflow earlier, but Vercel is now serving `index.html`. Any future edits should be made in `index.html` to ensure changes appear on the deployed site.

## Recent Work Completed

### Content and imagery

- Replaced remote stock image usage with local files in `images/`
- Updated imagery to better reflect Muslim community representation
- Adjusted program images to better match section meaning
- Updated testimonial avatars to more natural real-photo portraits
- Swapped the youth and volunteer cards to more colorful images

### Contact section

- Replaced the placeholder address panel with an embedded Google Map
- Kept the address and external Google Maps link below the embedded map

Map location used:

- `45 Delawney St, Balcatta WA 6021`

## Deployment Setup

The site is deployed with Vercel.

Current `vercel.json`:

```json
{
  "cleanUrls": true
}
```

### Deploy command

```powershell
npx vercel --prod --yes
```

### Live verification

The site was last verified to return:

- `200 OK`

Current production alias:

- `https://clad-website.vercel.app/`

## Image Management

Images are now stored locally in:

- `images/`

The HTML references those files directly with relative paths like:

```html
<img src="images/example-image.jpg" alt="Description" loading="lazy">
```

If an image needs to be replaced:

1. Add or replace the file inside `images/`
2. Update the matching `src` in `index.html`
3. Redeploy to Vercel

## Key Project Decisions

- Keep the site as a static single-file HTML site for simplicity
- Use local image assets instead of hotlinking remote image URLs
- Use `index.html` as the single source of truth
- Keep deployment simple through Vercel with no build step

## Recommended Next Steps

### High priority

- Delete `main.html` if it still exists outside the current active deploy flow
- Add Git commits if version history is needed going forward
- Review the site on mobile and desktop after each major content change

### Nice to have

- Move large inline styles into a more organized CSS section or external stylesheet
- Clean up old encoding artifacts if any remain in text content
- Consolidate any duplicated structured data / schema markup
- Add a favicon and final social share image audit

## Editing Guide

For future updates:

1. Open `index.html` in `C:\Users\User\Desktop\CLAD Website_2026-05-04`
2. Make content, layout, or image-path changes
3. Check any linked files in `images/`
4. Deploy:

```powershell
npx vercel --prod --yes
```

5. Confirm live site:

- `https://clad-website.vercel.app/`

## Handoff Summary

The website is live, image assets are local, the Google Map has been embedded, and the latest colorful image updates are deployed. Future work should continue from `index.html` inside `CLAD Website_2026-05-04`.
