# Chicago Image Generation Manifest

Source of truth for what needs Nano Banana 2 generation vs. what's reused free.
Built from visual audit (not filename guessing) of every recurring image category
across the SLC homepage + 5 city pages, 2026-08-25.

## REGENERATE for Chicago (16 images, Nano Banana 2) — REVISED for 1-main-page architecture

### Hero images (2 total — NOT one per suburb, per architecture decision)
- [x] Homepage hero (downtown Chicago skyline, golden hour) — PROTOTYPE TESTED,
      quality confirmed excellent (Willis Tower, Trump Tower, Buckingham
      Fountain all correctly rendered)
- [ ] Chicago main city page hero
- [ ] Service Areas directory page hero (generic Chicagoland/suburbs image —
      could reuse homepage hero or generate a wider "Chicagoland region" shot)

### Homepage cards (~5)
- [ ] commercial-card (was: Nine Penn Center, Philadelphia — named building)
- [ ] government-card (verify — likely fine, low priority check)
- [ ] residential-card (verify)
- [ ] specialty-card (verify)
- [ ] how-it-works-installation (installer wearing "WINDOW FILM PHILADELPHIA" shirt + skyline bg)

### Shared regional-context shots (4) — used across all city pages
- [ ] urban-heat (aerial Philly rowhome neighborhood + skyline — needs Chicago aerial equivalent)
- [ ] residential-rowhouses (Main Line PA stone rowhouse street — needs Chicago housing stock: three-flats/bungalows)
- [ ] commercial (storefront strip with "UPPER DARBY / 69TH ST" sign visible — needs Chicago commercial strip)
- [ ] gallery-restaurant (East Coast brick streetscape through restaurant window)

### Brand/product shots needing regen (7 of 12 — confirmed via individual visual check)
- [ ] brand-3m (rowhouse street visible through office window)
- [ ] brand-llumar (stone rowhouse street through window)
- [ ] brand-madico (brick rowhouse block through window)
- [ ] brand-graffiti-shield (explicit Philly brick storefront + pedestrian reflection)
- [ ] brand-vista (stone East Coast house through window)
- [ ] brand-casper (explicit Philly brick storefront street)
- [ ] brand-solargard (rowhouse street through window)

### Borderline — recommend regen for quality/consistency (3)
- [ ] app-homes (Tudor-stone building, East-Coast-coded)
- [ ] testimonial-residential (stone rowhouse visible through window)
- [ ] gallery-residential (brick rowhomes visible through window)

## REUSE AS-IS — zero cost (19 images)

### Confirmed generic/reusable category shots (11)
- film-decorative (frosted glass partition, generic office)
- gallery-solar-office (generic office park view, no skyline)
- expert-interior (generic cozy living room, no exterior visible)
- resources-meeting-room (generic office meeting, unrecognizable blur)
- gallery-privacy-medical (generic hospital corridor)
- app-government (generic civic building)
- brand-huper-optik (generic office exterior)
- brand-solyx (generic frosted glass door)
- brand-hanita (generic glass tower exterior)
- brand-hdclear (generic glass office corridor)
- brand-cbond (generic office corridor)

### Team photos — REAL, verified via vision check (8)
All from windowfilmphiladelphia.net/about/team — genuine staff photoshoot,
consistent studio lighting/backdrop, natural asymmetry, "Scottish Window Tinting"
branding visible on 2 of 8. Confirmed reusable across ALL city sites.
- Martin Faith (Founder/CEO)
- Mike Kinsey
- Katie Pelowich
- Travis Thompson
- Blake Parish
- Cannon Russell
- Kelly Escorcia
- Shanna Sweet

Real founder story (usable, factual): Martin Faith, from Glasgow, Scotland,
started as a stained-glass artisan, moved into window film in 2008 after
tracking his own utility savings ($8.98/day -> $2.54/day). 30+ years in home
improvement. "Since 2008" claim is REAL — do not remove, do reuse the framing.

## Not yet audited (low priority — verify before Chicago launch, not blocking)
- Remaining ~140 images referenced across non-homepage/non-city pages
  (products, benefits, applications, resources subpages)
- Recommend spot-check pattern before full site regen: same "brand-*" and
  "*-hero.jpg" naming patterns are highest-risk for hidden regional content

## Cost estimate — CONFIRMED via /estimate endpoint (2026-08-25), revised 2026-08-26
Nano Banana 2 text-to-image pricing (per image):
- 1K: $0.08/image (1.280 credits)
- 2K: $0.12/image (1.920 credits) — recommended for hero/card shots
- 4K: $0.16/image (2.560 credits)

Revised total: ~16 images needed (2 hero + 5 cards + 4 shared-regional +
7 brand-with-regional-context, minus overlap) = **~$1.92 at 2K, ~$2.56 at 4K.**
Cheaper than the original 24-image/5-city-page estimate because the
1-main-page + directory architecture eliminates 22 of the 24 suburb hero
images that would otherwise be needed.

Account has 1,400+ credits (~$87+ worth at 2K pricing) — Chicago uses under
2% of available balance.

Failed and "nsfw"-flagged requests are NOT charged (confirmed in Higgsfield
billing docs) — false-positive content-filter rejections cost nothing, only
successful generations are billed. No waste-rate budgeting needed.
