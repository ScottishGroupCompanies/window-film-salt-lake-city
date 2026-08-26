# Chicago Site Configuration Manifest

The swap manifest for everything that varies by city (non-image). Fill in the
blanks, then this becomes GLM's structured content brief input + the site.ts
config for the build.

## REQUIRED — cannot proceed without these

- [ ] Business/domain name: `windowfilmchicago.com`? or different brand name for Chicago?
- [ ] Phone number (real, Chicago-area)
- [ ] Email (e.g. contact@windowfilmchicago.com)
- [ ] Physical address / service base (if any — many of these sites don't
      publish a street address, just service area)
- [ ] Service area cities/neighborhoods (need 5, matching the SLC pattern of
      1 "main" city page + 4 satellite cities) — e.g. Chicago, Naperville,
      Evanston, Oak Park, Schaumburg? Your call on which submarkets matter.
- [ ] Google Business Profile — exists yet? (SLC said no — same question here)
- [ ] Facebook / social links — same Scottish Group Facebook, or Chicago-specific?
- [ ] "Since [year]" claim — reuse real 2008 founding story (verified real,
      see CHICAGO-IMAGE-MANIFEST.md) or does Chicago market position as a
      newer expansion of the same company?

## Derived from real, reusable facts (no new input needed)
- Founder story: Martin Faith, Glasgow-born stained-glass artisan -> window
  film in 2008, real utility savings data ($8.98/day -> $2.54/day)
- Team roster: 8 real staff (see image manifest) — reuse across sites
- Manufacturer partnerships: 3M, LLumar, Vista, Solar Gard, Huper Optik,
  Madico, Solyx, HDClear, Hanita, Graffiti Shield, C-Bond, Casper — same
  everywhere, no swap needed
- NFRC / manufacturer citations — same everywhere

## Regional facts GLM needs for authentic (not generic) Chicago content
- [ ] Climate framing: Chicago = Zone 5A, brutal winters + humid summers +
      lake-effect weather — NOT Utah's dry heat, NOT Philly's mixed-humid.
      Confirm before GLM writes — this was a real error source on SLC
      (inherited Philly's climate stats wrongly).
- [ ] Architecture vernacular for "residential-rowhouses" equivalent —
      Chicago = two-flats, three-flats, bungalows (Chicago bungalow belt),
      NOT East Coast stone rowhouses. Feeds both content AND image prompts.
- [ ] Neighborhood names for "trust-installer"/"gallery" contextual copy —
      need real Chicago neighborhoods (Lincoln Park? Wicker Park? the Loop?)
- [ ] Local landmarks for schema/geo data — Willis Tower, Millennium Park,
      Chicago River (tested successfully in image generation already)
- [ ] Transit reference — Chicago = "the L" / CTA (NOT SEPTA — this was a
      literal find/replace bug on SLC, must get city-correct name right
      the first time, not discovered via 8-pass rebuild like last time)

## Known past-error checklist (do NOT repeat on Chicago)
- [ ] No fabricated stats (SLC caught "4.9-star Google rating," "2,400
      projects" — these were UNVERIFIED template carryovers, removed).
      Chicago launches with ZERO invented numbers unless client confirms real.
- [ ] No leftover old-city text in JS string literals (caused 2 build
      breaks on SLC from unescaped apostrophes in replaced text — QA the
      GLM output against this before merging)
- [ ] Map embeds: must use REAL Chicago-area lat/lon per neighborhood page,
      not copy-pasted coordinates from another city (this broke silently
      on SLC — city pages showed the wrong city's map for days)
- [ ] Image filename bug: if the swap script renames `<img src>` paths in
      code, it MUST also rename/copy the actual files on disk in the same
      operation. This exact bug caused 1,088 broken images on SLC. Any
      Chicago swap script must do both in one atomic step with a post-swap
      "broken link" verification pass before considering the job done.

## Open questions for Jenny (blocking GLM content brief)
1. What are the 5 city/neighborhood pages for Chicago?
2. Real phone/email for Chicago?
3. Same Facebook page (Scottish Group) or new one for Chicago?
4. Keep "since 2008" framing, or Chicago is positioned as a newer market entry?
5. Any real Chicago testimonials/reviews yet, or launch without (same as SLC)?
