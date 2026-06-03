# Changelog — nis2-navigator

All notable changes to this skill are documented here.

Format: `## [vX.Y] — YYYY-MM-DD`

---

## [v1.1] — 2026-05-31

Currency fix for the German national profile.

- **KRITIS-Dachgesetz status.** `references/germany-nis2umsucg.md` corrected: the KRITIS-Dachgesetz (CER Directive implementation) is no longer "expected to enter into force in 2026" — it **entered into force on 17 March 2026**. Same pending-resolved pattern as other recently-enacted German implementing laws.

No change to the assessment method, scope logic, or other jurisdiction profiles. The German NIS2UmsuCG (BSIG-neu) in-force date (6 December 2025) and the 6 March 2026 registration deadline were already correct.

**Status:** reviewed (carried from v1.0).

---

## [v1.0] — 2026-05-14

First **reviewed** release. Eval pass via `/skill-creator` confirmed skill value against no-skill baseline.

- 4 realistic test cases run with-skill vs no-skill baseline (32 assertions total)
- Result: 31/32 (96.9%) with skill vs 17/32 (53.1%) without — **+43.8 pp differential**
- Diagnostic finding: baseline misclassified the case 1 cloud-provider as "essential" (skill correctly identified as important under Annex I + medium); skill cited § 38(2) BSIG personal liability, CIR 2024/2690, 6 March 2026 deadline, BSI-Standards 200-2/200-3, ISO 27001:2022 Annex A mapping where baseline missed these
- Eval-assertion bugs identified for iteration-2 patch: assertions citing "§ 30 BSIG" for BSI registration should reference § 33 BSIG-neu (§ 30 covers risk management measures); the with-skill output correctly cited § 33
- See `../../nis2-navigator-workspace/iteration-1/` for full eval artifacts

## [v0.9] — 2026-05-08

Initial import from /CLAUDE_PROJECTS/SKILLS/nis2-navigator/ (worked on 2026-03-26). Status: **pre-review** pending eval.

- NIS2 Compliance Navigator under EU Directive 2022/2555
- Scope classification (essential vs. important entities, Annex I/II)
- Art. 21 gap analysis with 0-4 maturity scoring
- Compliance roadmap generation
- Deep German BSIG-neu / NIS2UmsuCG coverage; profiles for Italy, France, Netherlands, Austria, Spain
- Triggers on NIS2, BSIG, BSIG-neu, NIS2UmsuCG, Cyberbeveiligingswet, Loi Résilience, NISG, decreto legislativo 138
