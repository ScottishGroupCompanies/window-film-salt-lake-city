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
24 cities/suburbs, NOT 24 full pages. Structure:
- **1 main "Chicago" page** — full page, own hero, full local content
  (same depth as SLC's salt-lake-city.astro)
- **1 lightweight "Service Areas" directory page** — lists all 24 cities as
  a service-area index/directory (like SLC's cities.astro overview page),
  NOT individual dedicated pages per suburb
- Rationale: 24 individual pages would be disproportionate SEO/content
  effort for suburbs; the directory approach is faster, cheaper, and still
  captures "near me" search intent without diluting content quality

Full city list (24):
Arlington Heights, Aurora, Berwyn, Bolingbrook, Chicago, Cicero, Des Plaines,
Elgin, Evanston, Gary, Joliet, Kenosha, Mount Prospect, Naperville, Oak Lawn,
Oak Park, Orland Park, Palatine, Racine, Schaumburg, Skokie, Tinley Park,
Waukegan, Wheaton

Note: Gary, Kenosha, Racine are in IN/WI, not IL — confirm these are
intentional (multi-state service area) before writing city/state metadata
into schema.org LocalBusiness markup (areaServed).

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

## Open / still needs confirmation
- [ ] Google Business Profile — exists for Chicago yet, or launch without
      (same as SLC, which launched with no GBP and hidden review badges)?
- [ ] Facebook — same Scottish Group page as other sites, or Chicago-specific?
- [ ] Real Chicago testimonials — none yet confirmed; launch without
      fabricated reviews (same rule as SLC)
- [ ] Confirm windowfilmchicago.com is the actual domain to build toward

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
