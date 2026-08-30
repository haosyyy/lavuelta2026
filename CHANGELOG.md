# Changelog — La Vuelta a España 2026 stage tracker

All notable changes to this page are documented here. Newest first.

Sections follow [Keep a Changelog](https://keepachangelog.com/) conventions:
**Added** for new features, **Changed** for changes to existing behaviour,
**Fixed** for bug fixes, and **Known limitations** for things that are
deliberately incomplete or still unverified.

## 2026-08-30 — verification pass

### Fixed

- **Stage 5's winning time was wrong by exactly ten minutes.** The page carried `3:57:12`; the official ranking at lavuelta.es gives **3:47:02**. The error was caught by arithmetic before the network: Pogačar finished in the bunch that day, so his GC total after stage 4 (7:38:59) plus the stage time must equal his GC after stage 5 (11:26:01) — and 7:38:59 + 3:47:02 is 11:26:01 exactly, with zero bonus seconds, as it should be for a rider who took none. `3:57:12` overshot by 610 seconds.

### Changed

- **Every podium and finishing time on the page is now checked against the official rankings at lavuelta.es**, stage by stage. Stages 1, 2, 4, 6, 7 and 8 matched what was already published; stage 3 is confirmed by the official page returning "no rank available", which is what a cancelled stage should look like.
- **Winner's times filled in for stages 7 and 8** — `3:49:47` for Leknessund and `3:47:06` for Coquard. These had deliberately been left blank because no source at the time gave them; the official rankings do.
- Footer now records that podiums and times are verified against the official rankings, with the date of the last check, and no longer claims a stale "last checked after Stage 5" while carrying results through stage 8.

### Known limitations

- **Official route distances disagree with the pre-race route table** on at least two stages: lavuelta.es gives stage 2 as 200.1km (table says 215.2) and stage 8 as 161km (table says 176.4). The table is pre-race published data and feeds the ribbon widths and the total-distance stat, so it has been left alone rather than changed as part of a results check.
- **Classification point totals are not from the official site.** The official rankings pages serve their stage results to a fetch but not their points/mountains tables, so those figures still come from race reports. The margins reconcile across stages (82 to Brennan's 60 after stage 5; a 33-point lead after Pogačar won stage 6), but they are not officially sourced the way the podiums now are.
- **Some stage-5 narrative detail is unverified** — the named five-man break and the lead-out description came in via a merge and were not checked against a source in this pass.

## 2026-08-30

### Added

- **Stage 8 — Pogačar crashes out, and the page says so.** A 💔 marker sits beside the route name in the running order (with an `aria-label` naming what it means), and the stage detail leads with a `.result-void` panel rather than the podium: around 31km from Xeraco he brushed shoulders with another rider, went down on his shoulder and face, tried to remount and walked to the ambulance. Concussion, a displaced left clavicle fracture, a stable C7 fracture and multiple abrasions; he abandoned 3:50 in the lead, the first Grand Tour he has failed to finish. **Bryan Coquard (Cofidis)** won the sprint for the first Grand Tour stage of his career at 34, and **Enric Mas** inherited red — the first Spaniard to lead the Vuelta since Jesús Herrada in 2018.
- **Stages 5, 6 and 7.** Brennan's second win in Roquetes off a Visma lead-out; Pogačar's third in six days at Castelló, won in a sprint from Mas after running off the road on the Puerto El Bartolo gravel descent; and an emotional Uno-X one-two at Aramón Valdelinares on the day King Harald V died, Leknessund going clear with 7.5km left for his first Grand Tour win. Stage 5 was filled in as well as the stages that were asked for, so the running order has no gap.
- **The jerseys moved a lot across these four days.** Pogačar held red, green and the polka dots through stage 6; Van Aert took the points classification outright on stage 7 and Leknessund the mountains, ending the triple; after stage 8 all four jerseys sit on different riders for the first time in the race — Mas, Van Aert, Leknessund and Onley — so no card needs a "worn on the road by" line.

### Known limitations

- **Winning times are shown only where a source gave one.** Stages 5, 7 and 8 list the podium without the winner's finishing time rather than carrying a guessed one; the gaps and `s.t.` markers are unaffected.

## 2026-08-26

### Added

- **Stage 3 — cancelled, and shown as cancelled.** A hailstorm caught the reduced bunch on the Col de Mont-Louis about 20km from the summit finish; Pogačar rode to the front, waved the group down and pointed it off the course, and the stage was abandoned rather than restarted. The stage carries a `.result-void` panel in place of a podium — striped like the rest-day rows — and a muted `Cancelled` chip instead of a winner chip. No times or climbing points were recorded, so its jersey cards repeat stage 2's and say so.
- **Stage 4 result — Andorra la Vella.** Pogačar went alone with 50km left over the Coll d'Ordino and the Collada de Beixalis and won by 2:39 from Jarno Widar and Felix Gall. He now leads red (7:38:59, Roglič +3:21, Mas +3:32), green (82 pts) and the mountains (23 pts); Oscar Onley takes white, up 15 places.
- **"Worn on the road by" line on jersey cards** (`.jw`). When one rider leads several classifications the jersey is worn by the next rider down, and after stage 4 that is three of the four: Pogačar leads red, green and polka dots, so Ethan Hayter rides in green and Lorenzo Fortunato in the polka dots. The line is deliberately one of the few things kept when the top panel clones a card — without it "In the jerseys" would have shown Pogačar three times over and been wrong about who is actually wearing what. Back-filled onto stages 1–3, where Hayter was already wearing green.

### Changed

- The "In the jerseys" panel now reflects stage 4, again with no edit of its own.

## 2026-08-24

### Added

- **Stage 2 result — Monaco → Manosque.** Matthew Brennan (Team Visma | Lease a Bike) won the uphill sprint at 21, on his Grand Tour debut, from Pau Miquel and Tadej Pogačar on the same time. Wout van Aert attacked inside the last 2km with Pogačar on his wheel before the move was swallowed up.
- **Jersey holders after stage 2.** Pogačar keeps red (4:58:40, Van Aert +0:09, Brennan +0:10) and leads green on 42 pts; **Koen Bouwman (Team Jayco AlUla) is the first mountains leader** with 6 pts over the day's two cat.3 climbs, so the polka-dot card is no longer "Not yet awarded"; Brennan takes white off Josh Tarling. Ethan Hayter briefly held red on the road on bonus seconds before losing it in a split in the finale.
- **A short race-narrative line under each stage podium** (`.result-note`), saying how the stage was actually won. Added to stage 1 as well, so every result block reads the same way.

### Changed

- The "In the jerseys" panel at the top of the page now reflects stage 2 — no edit was needed there, which is the point of deriving it from the stage list.
- Footer credits Cyclingnews and Cycling West alongside the existing results sources.

## 2026-08-23

### Added

- **Stage results and jersey holders.** Each completed stage now carries a result block in its detail panel: the stage podium (top three, with teams and gaps) and the four classification leaders after that stage — red (general classification, Carrefour), green (points, Škoda), white with blue polka dots (mountains) and white (best young rider). Stage 1's Monaco time trial is in: Tadej Pogačar by 0.09s over Ethan Hayter, with Josh Tarling third at four seconds; Pogačar in red and green, Tarling in white, and no mountains leader yet.
- **"In the jerseys" section at the top of the page**, directly under the race callout, showing who is in each of the four jerseys right now and what each classification is awarded for. It is *derived* — built at runtime by cloning the four jersey cards from the last stage in the running order that has a result — so recording a new stage means editing one place in the stage list and nothing at the top. It stays hidden until a stage has been ridden, and again after the final stage it reads as the final classifications.
- **Winner chip on completed stage rows**, so the running order shows who won each stage without opening it.

### Changed

- **The "Live results" section no longer disclaims tracking results.** It now explains that podiums and jersey holders are recorded per stage and summarised at the top, and points to lavuelta.es for live timing and the full classifications rather than for everything.
- **Footer and contender copy corrected for a race that has started** — the footer no longer says "the 2026 Vuelta a España has not yet started", the contender notes are labelled as a pre-race snapshot that is not revised stage by stage, and the results sources are credited alongside the route sources.
- Page description and Open Graph / Twitter card text mention results and jersey holders.

### Known limitations

- **Results are entered by hand after each stage, not live.** There is no feed behind them; between the finish and the next edit the page is out of date, and during a stage it shows the previous stage's jerseys.
- **Only the stage podium is listed.** Sources disagreed below third place on Stage 1, so positions 4 and beyond are deliberately not claimed. Full classifications stay on lavuelta.es.
- **The mountains classification had no leader after Stage 1** — the Monaco circuit had no categorised climbs, so that card reads "Not yet awarded" until Stage 2.
- **The "In the jerseys" section needs JavaScript.** It is cloned from the stage markup at runtime, so it is hidden in the `noscript` fallback — but each stage's own result block is static markup and stays fully readable without JS.

## 2026-08-22

### Added

- **Today's stage is highlighted in the running order.** The current stage's row gets a warm red wash, a red stage number and date, and a `TODAY` pill next to the route name; its expanded detail panel picks up a matching tint. On a rest day the rest-day stripe is highlighted instead. "Today" is resolved in Singapore time, so the highlight is correct regardless of where the page is being read.
- **"Jump to today's stage" button** in the callout at the top of the page, shown whenever a stage is being ridden today — including on race morning while the countdown to the first rider off is still running. It opens today's stage and scrolls to it, and clears an active terrain filter first if that filter is hiding today's stage. The existing floating "Back to Today" button now only appears once both today's stage *and* the callout are off screen, so the page never offers the same action twice at once.
- **Live race states for the callout.** The Grand Départ countdown is now one of four states, chosen from the date: counting down before the start, today's stage (number, distance, terrain) while racing, a rest-day panel naming tomorrow's stage, and a finished state after Granada.
- **Hollow climb markers** for named climbs the organisers haven't categorised. Two variants: *category to be confirmed* and *uncategorised*. This puts markers on the summit finishes of Stages 3 (Font Romeu), 7 (Aramón Valdelinares), 12 (Calar Alto) and 14 (Sierra de la Pandera), the final climb of Stage 10 (Puerto de Socovos), and the five Alhambra ascents of Stage 21 — all of which previously rendered as bare lines. Both variants are explained in the legend above the stage list.
- **Ribbon segments are interactive.** Each of the 21 segments is now a real button: keyboard focusable, with a full aria-label, the shared tooltip on hover/focus, and click-to-open-that-stage (clearing an active filter if needed).
- **`<meta name="description">` and Open Graph / Twitter card tags**, so the page no longer shares as a bare URL.
- **`noscript` fallback.** The ribbon, profiles, countdown and accordion are script-driven; without JS the page now falls back to a plain, fully readable stage list instead of leaving every stage detail permanently collapsed.
- This changelog.

### Changed

- **Stage data now has a single source of truth.** It previously lived in three hand-maintained copies — the ribbon segments, the accordion rows, and the `stageDates` map in JS. The accordion markup is now the only copy; the ribbon, the summary stats, the filter counts and the date lookups are all derived from it at runtime. A stage can be edited in one place without the page drifting out of sync.
- **Readability pass over the body copy.** Type sizes raised throughout the non-heading content — stage rows 14 → 15.5px, stage notes 12.5 → 13.5px, expanded detail 13.3 → 14.5px with detail values at 15px, card and rider copy 13.8 → 15px, section intros 14.5 → 15.5px, footer 11.5 → 13px, profile captions 10 → 11.5px. Monospace micro-labels (dates, distances, terrain, field labels) moved from weight 400 to 500, and prose line-height from 1.5 to 1.6. Detail columns widened from a 190px to a 215px minimum so climb lists stop wrapping every couple of words.
- **`--ink-soft` `#5E5647` → `#544C3F` and `--ink-faint` `#8A8171` → `#6B6153`.** `--ink-faint` was carrying the smallest text on the page at a 3.15–3.41:1 contrast ratio, below the WCAG AA 4.5:1 minimum on every surface. All 49 distinct text styles on the page now meet AA.
- **Total distance is computed from the stage data** (3,291 km) rather than hard-coded, with a note recording the organisers' headline figure of 3,275 km.
- The ribbon no longer clips its children, so focus rings on its segments stay visible; the rounded ends moved onto the end segments themselves.

### Fixed

- **Rest days ignored the terrain filter.** Filtering to a single terrain left the two rest-day stripes stranded between unrelated stages.
- **Collapsed stage panels stayed in the keyboard tab order.** The accordion only collapses visually (`grid-template-rows:0fr` + `overflow:hidden`), so every climb-profile dot in all 21 closed stages was still focusable — a keyboard user tabbed through the entire race before reaching the next control. Closed panels are now `inert`.
- **`prefers-reduced-motion` was overridden by the JS.** The stylesheet set `scroll-behavior:auto` under the reduced-motion query, but `scrollIntoView({behavior:'smooth'})` passed `smooth` explicitly, which wins. Scroll behaviour is now chosen from the media query.
- **The load-time auto-scroll hijacked the viewport** unconditionally, 450ms after load, on every visit during the race. It now stands down if the reader has already scrolled or interacted, if there is a URL hash, or on a back/forward restore.
- **The countdown pinned at zero once the race started** and the callout kept advertising the Grand Départ for the following three weeks. Superseded by the live race states above.
- **Climb markers on a chart's first or last point were clipped** by the SVG viewBox — including the Categoría Especial dot on Stage 20's summit finish. Profile padding now accounts for the largest marker.
- **The climb tooltip could render off the top of the viewport** with no flip, and mis-measured its own width: it is `position:fixed` with `left` set and `right:auto`, so its shrink-to-fit width depended on wherever it was last placed, which mis-clamped it near a viewport edge. It now measures from a neutral position, pins its width, and flips below the target when it will not fit above.
- **Resize rebuilt all 21 profile SVGs on every resize event.** Marker updates are coalesced per animation frame, and profiles only redraw on an actual width change — so height-only changes (a mobile URL bar sliding away) cost nothing.
- **Total distance disagreed with the stage list**: the stats bar said 3,275 km while the 21 listed stages sum to 3,291.3 km.
- Filter buttons had no `aria-pressed` and no group label; ribbon segments were `div`s whose only affordance was a `title` attribute, invisible to touch and keyboard.

### Known limitations

- **Climb profiles are schematic, not GPX data.** The shapes are hand-authored 0–1 elevation curves that convey a stage's character; they are not surveyed profiles, and marker positions along the x-axis are approximate.
- **Start and finish times are estimates**, derived from typical Vuelta scheduling per stage type, not official timings. The countdown targets an estimated first-rider-off of ≈22:45 SGT on 22 August (≈16:45 CEST in Monaco).
- **The 3,275 km vs 3,291.3 km discrepancy is unresolved.** The page shows the sum of the published stage distances and footnotes the organisers' figure; which of the two is authoritative is not something this page can settle.
- **Several climb categories are still unpublished.** Stage 6's climb list was not reliable enough to mark at all and carries no dots; the summit finishes on Stages 3, 7, 12 and 14 are marked as "category to be confirmed" rather than assigned a category.
- **Elevation gain is `TBC` for several stages**, including Stages 12 and 21, and Stage 1 has no published figure.
- **No live results.** Stage results and jersey standings are deliberately out of scope and link out to lavuelta.es.
- **Contender notes reflect pre-race form and team news** as reported ahead of the Grand Départ, not confirmed results.
- **Light theme only.** The page sets `color-scheme: light` and has no dark-mode palette.

## 2026-08-21 and earlier

Initial build and pre-race updates, recorded in git history rather than here:
the stage list, distance ribbon and bike marker, terrain filters, climb
profiles with category dots, the Grand Départ countdown, contender cards, and
the link-out to official rankings.
