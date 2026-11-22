# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This is a content project, not a software project. The goal is to create a slide deck for Raj Madhuram's Day 1 lecture — **Session 3: "Problem to Solution"** — at the PRARAMBH Deep Dive Workshop (28–30 August 2026, SRM University AP), a 3-day event where 34 student venture teams are mentored from idea to pitch readiness.

The session's scope (from the mentor guide): Ideation Techniques, Solution Design, Value Proposition Canvas, Feasibility Analysis, Opportunity Evaluation, MVP & Prototype Development. Expected outcome: students connect their solution to a validated problem and adopt a practical, testable MVP approach.

## Source documents

- `Mentor Guide- PRARAMBH Deep Dive Workshop (1).docx` — workshop structure, all four Day 1 sessions, mentoring frameworks, pitch deck sequence students must follow.
- `responses-1.xlsx` — the AUTHORITATIVE team roster as of 29 Aug: use its "Final" sheet (34 rows, 31 unique teams — Revolution Royals ×3, saffron team listed as both Trinetra and Trientra). Haven was added; Cauframe, Innovators, Gagan, OpenBin were dropped (parked in Sheet1 along with Astroclean). Dream It is agri per Raj, despite the sheet saying med tech.
- `PRARAMBH- Deep dive 2026 -PPT (Responses).xlsx` — older submissions snapshot (36 rows, 34 unique teams), superseded by responses-1.xlsx. Its `Raj` column flags conflicts of interest (SNFS: CoI; Green Genesis: potential CoI).
- `PRARAMBH- Deep dive 2026 -PPT (Responses) - Form Responses 1.pdf` — same data as the xlsx, superseded by it.
- Raj's original "Joy of Building" talk (source for the deck's opening act): https://gamma.app/docs/St-Josephs-Aug-2026-tr5dowt2dtafeaw — Colour Genie, "What is your garage?", scratch-your-own-itch (Dropbox/Facebook/Ather), QuizStar story, hobby projects Pcaisso (pcaisso.vercel.app) and Fantasia (fantasia-v4.vercel.app). Blocked to WebFetch; read it via the Chrome browser tools.

Extracting content:
- docx → text: `textutil -convert txt <file> -output <out.txt>` (pandoc is not installed)
- xlsx/pdf: no system Python packages for these; create a venv and `pip install openpyxl pypdf`, then extract with a short script. `pdftoppm`/poppler is not installed, so the Read tool cannot render PDF pages — extract text instead.

## Audience facts worth keeping in mind

- Stage split: ~26 teams at Idea, 8 at Prototype, 1 at MVP (NeuroNest).
- Sector concentration: AgriTech (~5), Health/MedTech (~6), plus services, fintech, cybersecurity, sustainability.
- Submissions range from tightly scoped ideas (Aven, Stellaris/Veritas, NeuroNest) to broad "everything platforms" (Bio-OS, Desi9, HappyHome) — useful contrast material for teaching solution scoping and MVP thinking.

## Current status (28 Aug 2026)

The workshop approach changed twice. `slides1.html` is the active deck (21 slides), built incrementally exactly as Raj directs — a colleague now covers "why to build" and "what to build", so Raj's talk is "The Joy of Building …and how to build, in 2026": (1) why now, (2) the data model is the heart of the system (SRMPay as the worked ERD example), (3) building with AI (3D-modeler story), (4) two stories — Yahoo Moneyball sprint and the Hugging Face marathon (NVIDIA acquired HF for $12.9B, announced 27 Aug 2026). Copy style: straight to the point, no flowery language. `slides.html` (41 slides) is the earlier full Problem→Solution version, kept for reference/raiding.

## Decisions

- Lecture slot duration: ~90 minutes.
- Deck format: HTML deck in this repo (`slides.html` + `assets/` for images), presents offline in any browser; printable to PDF. `SPEAKER_NOTES.md` carries the timing map and talk track. `worksheet.html` is the printable A4 activity handout (one per team) for the end-of-session exercise.
- Examples: use the student teams' own submissions, named (no anonymization needed). Keep any critique-flavored examples (e.g., broad "everything platform" scoping) framed respectfully — as ambitious visions that need a first wedge, not as mistakes.
- Tone: practical and story-driven, not formal/theoretical. The deck opens with Raj's "The Joy of Building" segment (his EACA Colour Genie story — assets/colour-genie.jpg, CC BY-SA 3.0, credit Frank Seger/Wikimedia). Personal stories woven in: Yahoo Project Moneyball (18 people, 43 days, Gemini, ~$300M yr-1; Raj was at Yahoo) and his GCT college 3D-modeling project re-created recently with Claude Code in hours. Paul Graham essays are a recurring thread (How to Get Startup Ideas, Schlep Blindness, Do Things That Don't Scale) with essay names cited on-slide. Software-biased MVP guidance is deliberate and owned on-slide; hardware teams get their own path.
- Raj's background (for slides/attribution): Co-Founder & CTO of C1X, 30+ years in software, ex-Yahoo!, MS from UCF, 3D graphics specialty. linkedin.com/in/rmadhuram.
