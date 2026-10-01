# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static HTML, CSS and JavaScript with no framework and no build step (`index.html`, `styles.css`, `main.js`). No React, Next.js or Tailwind. Motion with CSS and the Web Animations API, no heavy libraries. Fonts self-hosted in `assets/fonts/` via `@font-face`. Images in WebP, lazy-loaded, ideally under 300 KB each. Deploy target: GitHub Pages, free, no build step. Decided by the user in `prompt-personeria.md` and `CLAUDE.md`.

## Users

- **Primary:** students of the Colegio de María Auxiliadora (Barranquilla, Colombia). They open the page on a phone (360–390 px) from a link shared on WhatsApp or Instagram, usually in a short moment, and decide whether to take the campaign seriously.
- **Secondary:** teachers, school leadership (directivas) and families, who review it with more time and judge whether the proposals are serious and feasible.

## Product Purpose

The one-page campaign site for Juan José Barbosa (Grado 11) as candidate for *personero estudiantil*, period 2027, under the campaign name **Firmes por el Mauxi**. It presents the campaign and its proposals in four axes: I. Académico, II. Convivencial, III. Ambiental, IV. Cultural y Social.

Success: within 30 seconds a visitor understands what the campaign proposes and why to believe it can be done.

## Positioning

Every axis pairs long-range main proposals with *propuestas express*: concrete actions with no budget, executable in under two weeks, that can start in the first week. The campaign's claim is that it does real, visible things fast with free tools anyone can use from a phone, not empty promises. It is also tied to the school's road to its centenary (1927–2027) through the MAUXI100 living archive.

## Operating Context

- Shared as a link in WhatsApp and Instagram; the link preview (Open Graph) is the first impression.
- Read mostly on phones, in passing, between classes or at home; leadership and families may read on desktop.
- The school community has its own terms: "MAUXI" (the school), "voceras/voceros" (class representatives), "personería", "gabinete", "firmas" (disciplinary marks), "Pruebas Saber / Saber 11", "hermanas FMA", "Promoción 100".

## Capabilities and Constraints

- One page. Structure: campaign presentation (hero), four axes each with main proposals and *propuestas express*, a brief section on the shared free tools, and a closing.
- Main proposals are renumbered continuously 1–11 in reading order (the source numbering 1, 2, 9, 3, 4, 10, 5, 6, 11, 7, 8 is discarded).
- "Teatro Invisible" appears once only, as main proposal "Intervenciones Simbólicas de Consciencia Social" in Axis IV; the duplicate express item in Axis II is removed.
- The source's tools section ("Stack Tecnológico MAUXI 2027") stays, kept brief.
- Date correction confirmed by the user: "Cápsula del Tiempo 2027" refers to the students of **2027** and the sealing act in **December 2027** (the source says 2026 in both places). The letters are still to be read in 2077, the school's 150th anniversary.
- Copy may be shortened and polished for mobile without changing meaning; every change must be shown to the user.
- All source emojis are replaced by iconography.
- Quality floor: AA contrast, visible keyboard focus, semantic HTML, `alt` on all images, `prefers-reduced-motion` respected, Lighthouse ≥ 90 in performance and accessibility, Open Graph tags.
- Ask before deleting files, `git push`, or installing anything. Commit when the user approves an advance.

## Brand Commitments

- Campaign name is exactly **"Firmes por el Mauxi"** (2027). Any "Maux" in source material is an error to correct.
- Candidate: **Juan José Barbosa, Grado 11.**
- School: Colegio de María Auxiliadora, Barranquilla.
- Language: Spanish of Colombia, clear and direct, no empty propaganda language.
- Inclusive language: refer to the student body with neutral formulations ("el estudiantado", "cada estudiante", "la comunidad estudiantil", "quienes…"), avoiding both generic masculine and "-e"/"x" forms. The source mixes forms and must be normalized.
- Existing tagline in the source: "Rompiendo paradigmas para la Excelencia Integral" and footer line "Innovación, Excelencia y Consciencia Ciudadana". No other slogan has been provided.
- Binding visual direction is set in `prompt-personeria.md` §3–4 (recorded there, not here).

## Evidence on Hand

- `referencias/Firmes_por_el_Maux_2027_v2.html`: the full source copy for all proposals (use its text, not its design).
- `referencias/capturas/` is empty and `referencias/notas.md` is an unfilled template: there are no style screenshots or taste notes. The user chose to proceed from the written brief alone.
- `assets/fotos/` and `assets/logo/` are empty today. The user **will provide**: photos of the candidate, photos of the team, and the campaign's social accounts. Until they arrive, use clearly marked placeholders; never fabricate them.
- No campaign logo or school crest is available; a monogram or seal may be proposed. The school crest may only be used with permission.
- Absent and not to be invented: team member names, testimonials, endorsements, statistics, achievements, quotes, dates beyond those in the source.

## Product Principles

1. **Credibility over spectacle.** Every claim on the page comes from the source; feasibility (express actions, free tools, start dates) is the persuasive core.
2. **Thirty-second clarity.** The four axes and the express idea must be graspable at a glance on a phone before any detail.
3. **Heritage that serves a modern reader.** The school's centenary and tradition are real; navigation, legibility and speed must still feel current.
4. **Everyone included.** Neutral, respectful language for the whole student body, and access for every reader regardless of device or ability.

## Accessibility & Inclusion

WCAG AA contrast minimum (gold text only on blue or at large sizes, verified), visible keyboard focus, semantic landmarks and headings, descriptive `alt` text, `prefers-reduced-motion` honored, fast on mid-range phones over mobile data.
