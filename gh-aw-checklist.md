# GitHub Agentic Workflows — Build Checklist

For the **Microsoft Dev Days** demo. Uses a fork of `doctor-ew/atlaiweek-fifa`
(separate from the Atlanta AI Week repo — see Setup).

---

## Repo Setup

```bash
# 1. Fork the Atlanta repo into a new Dev Days repo
gh repo fork doctor-ew/atlaiweek-fifa \
  --clone \
  --fork-name devdays-fifa-navigator \
  --org doctor-ew

# 2. Enter the new repo
cd devdays-fifa-navigator

# 3. Confirm the remote is clean (should point to devdays-, not atlaiweek-)
git remote -v

# 4. Install the gh-aw CLI extension
gh extension install github/gh-aw
gh aw --version

# 5. Scaffold the agentic workflows directory
gh aw init
```

- [ ] Fork created at `github.com/doctor-ew/devdays-fifa-navigator`
- [ ] Cloned locally and `cd`'d in
- [ ] Remote verified — Atlanta AI Week repo untouched
- [ ] `gh aw --version` returns a version string
- [ ] `.github/workflows/` directory scaffolded
- [ ] Confirm GitHub Actions is enabled on the new repo (`gh repo view --web` → Settings → Actions)

---

## Reactive Intelligence — IssueOps

Maps to: **Slide 4 pattern 1 · Slide 16 mapping row 1**

- [ ] `gh aw new issue-clarifier`
      On issue opened → AI asks for repro details (mirrors the PPT's own slide 8 screenshot)
- [ ] `gh aw new pr-reviewer`
      On PR opened → AI reviews the diff, posts findings as a comment
- [ ] `gh aw compile` both
- [ ] Open a test issue and watch the bot respond ← **live stage demo**

---

## Continuous Improvement — TaskOps

Maps to: **Slide 4 pattern 2**

- [ ] `gh aw new dep-updater`
      Scheduled weekly → bundles Dependabot PRs into one
- [ ] `gh aw new simplify-check`
      On PR → flags overly complex functions (mirrors `/simplify` from gstack)

---

## Insight & Governance — DataOps

Maps to: **Slide 4 pattern 3**

- [ ] `gh aw new marta-api-health`
      Weekly → checks MARTA GTFS-RT + REST endpoints; opens an issue if they drift
- [ ] `gh aw new weekly-status`
      Every Monday → posts summary of open issues + stale PRs as a repo discussion

---

## Orchestration

Maps to: **Slide 4 pattern 4**

- [ ] `gh aw new release-notifier`
      On push to `main` → posts deploy summary comment linking to Vercel preview URL

---

## Stage Demo Prep

- [ ] Pick `issue-clarifier` as the live demo (low latency, matches PPT slide 8 exactly)
- [ ] Pre-stage a fake issue in a draft so you can open it in one click
- [ ] Have `gh aw logs issue-clarifier` ready to show execution trace after it fires
- [ ] Have `gh aw audit <run-id>` ready if something goes wrong on stage

---

## Slide mapping reminder

| Workflow | gstack analog | GitHub pattern |
|---|---|---|
| `issue-clarifier` | `/office-hours` | Reactive Intelligence |
| `simplify-check` | `/simplify` | Continuous Improvement |
| `marta-api-health` | `/plan-eng-review` | Insight & Governance |
| `release-notifier` | `/ship` | Orchestration |
| `dep-updater` | — | Continuous Improvement |
