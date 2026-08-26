# Chicago Site Configuration Manifest

CONFIRMED facts locked in 2026-08-26. This is the source of truth for the
GLM content brief and site.ts config.

## Business facts — CONFIRMED
- Phone: (773) 453-2005
- Email: contact@windowfilmchicago.com
- Domain: windowfilmchicago.com (assumed — confirm before DNS/Vercel setup)
- Founder story: REUSE Martin Faith / 2008 founding (real, verified — see
  CHICAGO-IMAGE-MANIFEST.md). Same company, Chicago is a market expansion,
  not a new brand — keep "since 2008" framing.
- Team: reuse the same 8 real staff photos + bios across all sites (Martin
  Faith, Mike Kinsey, Katie Pelowich, Travis Thompson, Blake Parish, Cannon
  Russell, Kelly Escorcia, Shanna Sweet)

## Service area architecture — DECIDED (differs from SLC's 5-city model)
20 IL cities/suburbs, NOT 20 full pages. Structure:
- **1 main "Chicago" page** — full page, own hero, full local content
  (same depth as SLC's salt-lake-city.astro)
- **1 lightweight "Service Areas" directory page** — lists all 20 cities as
  a service-area index/directory (like SLC's cities.astro overview page),
  NOT individual dedicated pages per suburb
- Rationale: 20 individual pages would be disproportionate SEO/content
  effort for suburbs; the directory approach is faster, cheaper, and still
  captures "near me" search intent without diluting content quality

Final city list (20, IL-only — Gary IN / Kenosha WI / Racine WI dropped
2026-08-26, out of state, not in scope):
Arlington Heights, Aurora, Berwyn, Bolingbrook, Chicago, Cicero, Des Plaines,
Elgin, Evanston, Mount Prospect, Naperville, Oak Lawn, Oak Park, Orland Park,
Palatine, Schaumburg, Skokie, Tinley Park, Waukegan, Wheaton

## Regional facts for GLM content (must get right — SLC learned this the
## hard way with Utah's climate/geography)
- Climate: Chicago = IECC Zone 5A, cold/snowy winters (lake-effect snow),
  hot/humid summers, high wind exposure (skyscraper wind-tunnel effect is
  a genuine, marketable angle for window film/security film)
- Transit: CTA / "the L" — NOT SEPTA (Philly), NOT UTA (Utah). Get this
  right in one pass, don't discover via 8-round rebuild like SLC.
- Architecture vernacular: Chicago two-flats, three-flats, courtyard
  apartments, Chicago bungalow belt — NOT East Coast rowhouses, NOT Utah
  suburban. Feeds both GLM content AND the image-generation prompts.
- Landmarks: Willis Tower, Millennium Park/Cloud Gate, Chicago River,
  Michigan Avenue, the Loop, Navy Pier
- Known regional pain points to build genuine content around: lake-effect
  glare off Lake Michigan, wind load on high-rise glass, winter heat-loss
  through single-pane vintage building stock, summer humidity + AC costs

## Confirmed launch posture — matches SLC's bare-bones launch pattern (2026-08-26)
- Domain: windowfilmchicago.com — confirmed good enough for now
- Google Business Profile: none yet — launch without, hide review
  badges/rating claims in footer (same pattern as SLC)
- Facebook: none yet for Chicago specifically — launch without, hide
  social link (same pattern as SLC)
- Testimonials: none real yet — launch with zero fabricated reviews
  (same rule as SLC — do not invent names/quotes/star ratings)

## Known past-error checklist (carried from SLC — do NOT repeat)
- [ ] No fabricated stats (no invented star ratings/project counts)
- [ ] No leftover old-city text in JS string literals (caused 2 build
      breaks on SLC from unescaped apostrophes)
- [ ] Map embeds use REAL Chicago-area lat/lon, verified per page, not
      copy-pasted from another city
- [ ] Any image-path rename in code MUST rename/copy actual files on disk
      in the same atomic step — this exact bug caused 1,088 broken images
      on SLC (found and fixed 2026-08-26, verified live)
- [ ] Post-swap verification pass: grep every <img src> reference against
      what actually exists in public/images before calling any city "done"
