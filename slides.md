---
theme: seriph
background: 'https://cxnebula71201.connexure.co/dropshare/Screen-Capture-2026-04-09-23-13-32-20260410031344-c4ff7f.png'
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## From Prompt to Production: Agentic Workflows in Practice
  Microsoft Dev Days · 2026
drawings:
  persist: false
transition: slide-left
title: From Prompt to Production — Agentic Workflows in Practice
mdc: true
defaults:
  background: 'https://images.unsplash.com/photo-1542831371-29b0f74f9713?w=1920&h=1080&fit=crop'
---

# From Prompt to Production

**Agentic Workflows in Practice**

<div class="mt-6 text-amber-400 font-semibold text-xl">Microsoft Dev Days · 2026</div>

<div class="mt-4 text-gray-300">Drew Schillinger · Enterprise Architect · @doctorew</div>

<div class="abs-br m-6 text-gray-400 text-sm">⚽ ATL FIFA Navigator · built in ~2 hours</div>

---
layout: statement
---

# The New Baseline

<div class="mt-8 space-y-5 text-left max-w-2xl mx-auto">

<div class="flex items-center gap-6">
  <div class="text-amber-400 font-mono w-14 shrink-0">2018</div>
  <div><span class="font-semibold">GitHub Actions</span> <span class="text-gray-300">— automation foundation. Scripts run on events.</span></div>
</div>

<div class="flex items-center gap-6">
  <div class="text-amber-400 font-mono w-14 shrink-0">2021</div>
  <div><span class="font-semibold">GitHub Copilot</span> <span class="text-gray-300">— editor assistance. AI as autocomplete.</span></div>
</div>

<div class="flex items-center gap-6">
  <div class="text-amber-400 font-mono w-14 shrink-0">2025</div>
  <div><span class="font-semibold">Copilot Coding Agent</span> <span class="text-gray-300">— SWE agents act on tasks. AI ships PRs.</span></div>
</div>

<div class="flex items-center gap-6 p-3 bg-amber-400/10 rounded-lg border border-amber-400/40">
  <div class="text-amber-400 font-mono w-14 shrink-0 font-bold">2026</div>
  <div><span class="font-semibold text-amber-400">GitHub Agentic Workflows</span> <span class="text-gray-300">— agents + Actions together. Technical Preview.</span></div>
</div>

</div>

<div class="mt-8 text-gray-400 text-sm text-center">The shift: from automation → intelligence</div>

---
layout: two-cols
---

# What GitHub Agentic Workflows Is

<div class="mt-4 space-y-4 text-sm">

<div class="p-4 bg-gray-800/80 rounded-lg border-l-4 border-amber-400">
  <div class="font-semibold text-amber-400 mb-2">Write it in Markdown</div>
  <div class="text-gray-300">Plain <code>.md</code> files with frontmatter. Triggers, AI engine, permissions, tools, env.</div>
</div>

<div class="p-4 bg-gray-800/80 rounded-lg border-l-4 border-blue-400">
  <div class="font-semibold text-blue-400 mb-2">The CLI</div>
  <div class="font-mono text-xs text-gray-300 mt-1 space-y-0.5">
    <div><span class="text-blue-400">gh extension install</span> github/gh-aw</div>
    <div><span class="text-gray-500">gh aw init</span>              <span class="text-gray-600"># set up repo</span></div>
    <div><span class="text-gray-500">gh aw new</span> my-workflow    <span class="text-gray-600"># create workflow</span></div>
    <div><span class="text-amber-400">gh aw compile</span>           <span class="text-gray-600"># .md → .lock.yml</span></div>
    <div><span class="text-green-400">gh aw run</span> my-workflow   <span class="text-gray-600"># execute</span></div>
    <div><span class="text-gray-500">gh aw logs</span>               <span class="text-gray-600"># view output</span></div>
    <div><span class="text-gray-500">gh aw audit</span> &lt;run-id&gt;    <span class="text-gray-600"># debug</span></div>
  </div>
</div>

<div class="p-4 bg-gray-800/80 rounded-lg border-l-4 border-green-400">
  <div class="font-semibold text-green-400 mb-2">Run in isolation</div>
  <div class="text-gray-300">Read-only permissions. Agent proposes actions. Threat detection scans output before execution.</div>
</div>

</div>

::right::

<div class="ml-6 mt-4">

```markdown
---
on: issues
  types: [labeled]
model: gpt-4o
permissions:
  issues: write
  pull-requests: write
tools:
  - github
---

When an issue is labeled "needs-repro",
investigate and open a draft PR with
a minimal reproduction case.
```

<div class="mt-4 text-xs text-gray-400 italic">*.md → gh aw compile → *.lock.yml → runs in CI</div>

</div>

---
layout: center
---

# The 5 Patterns — "Continuous AI"

<div class="mt-6 space-y-3 max-w-3xl mx-auto text-sm">

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-10 shrink-0 text-lg">1</div>
  <div>
    <div class="font-semibold">Reactive Intelligence</div>
    <div class="text-gray-300">ChatOps · IssueOps — AI responds to issues and PRs</div>
  </div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-10 shrink-0 text-lg">2</div>
  <div>
    <div class="font-semibold">Continuous Improvement</div>
    <div class="text-gray-300">DailyOps · TaskOps — scheduled AI-driven upgrades and self-review</div>
  </div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-10 shrink-0 text-lg">3</div>
  <div>
    <div class="font-semibold">Insight & Governance</div>
    <div class="text-gray-300">DataOps · ProjectOps — analyze data, update project state</div>
  </div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-10 shrink-0 text-lg">4</div>
  <div>
    <div class="font-semibold">Orchestration</div>
    <div class="text-gray-300">MultiRepoOps · CentralRepoOps — coordinate across repositories</div>
  </div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg border border-amber-400/30">
  <div class="text-amber-400 font-mono w-10 shrink-0 text-lg">+</div>
  <div>
    <div class="font-semibold text-amber-400">And more</div>
    <div class="text-gray-300">Design Patterns collection — the <span class="text-amber-400">Agentics</span> library · <span class="text-gray-400 text-xs">Peli's Agent Factory</span></div>
  </div>
</div>

</div>

---
layout: two-cols
---

# What Your CI/CD Can Do Now

<div class="mt-6 space-y-6 text-sm">

<div class="flex items-start gap-4">
  <div class="text-amber-400 text-xl w-6 shrink-0">→</div>
  <div>
    <div class="font-semibold text-lg">Understand context</div>
    <div class="text-gray-300 mt-1">Read the repository, issues & pull requests — not just predefined event payloads.</div>
  </div>
</div>

<div class="flex items-start gap-4">
  <div class="text-amber-400 text-xl w-6 shrink-0">→</div>
  <div>
    <div class="font-semibold text-lg">Make decisions</div>
    <div class="text-gray-300 mt-1">Choose what to do based on context — not just predefined conditions.</div>
  </div>
</div>

<div class="flex items-start gap-4">
  <div class="text-amber-400 text-xl w-6 shrink-0">→</div>
  <div>
    <div class="font-semibold text-lg">Stay on course</div>
    <div class="text-gray-300 mt-1">Understand concepts, not just GitHub primitives.</div>
  </div>
</div>

</div>

::right::

<div class="ml-6 mt-8 space-y-4">

<div class="text-gray-400 text-sm uppercase tracking-wider mb-4">Supported AI engines</div>

<div class="grid grid-cols-2 gap-3">
  <div class="p-3 bg-gray-800/80 rounded-lg border border-purple-400/40 text-center">
    <div class="text-purple-300 font-semibold">Copilot</div>
    <div class="text-gray-500 text-xs mt-0.5">GitHub · default</div>
  </div>
  <div class="p-3 bg-gray-800/80 rounded-lg border border-amber-400/40 text-center">
    <div class="text-amber-300 font-semibold">Claude</div>
    <div class="text-gray-500 text-xs mt-0.5">Anthropic</div>
  </div>
  <div class="p-3 bg-gray-800/80 rounded-lg border border-gray-400/40 text-center">
    <div class="text-gray-200 font-semibold">Codex</div>
    <div class="text-gray-500 text-xs mt-0.5">OpenAI</div>
  </div>
  <div class="p-3 bg-gray-800/80 rounded-lg border border-blue-400/40 text-center">
    <div class="text-blue-300 font-semibold">Gemini</div>
    <div class="text-gray-500 text-xs mt-0.5">Google</div>
  </div>
</div>

<div class="mt-4 text-xs text-gray-500 italic">Switch engines with one frontmatter field: <code class="text-gray-400">engine:</code></div>

</div>

---
layout: statement
---

# The Practitioner Gap

<div class="mt-10 grid grid-cols-2 gap-12 max-w-2xl mx-auto text-left">

<div class="space-y-3">
  <div class="text-amber-400 font-semibold text-sm uppercase tracking-wider">GitHub defines</div>
  <div class="text-lg">The agentic future.</div>
  <div class="text-gray-300 text-sm">5 patterns. A platform. A vision for what CI looks like when AI does the work.</div>
</div>

<div class="space-y-3">
  <div class="text-amber-400 font-semibold text-sm uppercase tracking-wider">You need</div>
  <div class="text-lg">A way there. Today.</div>
  <div class="text-gray-300 text-sm">Before your org adopts Agentic Workflows. Before the preview ships to everyone.</div>
</div>

</div>

<div class="mt-12 text-center text-xl">
  <span class="text-gray-300">The practitioner's toolchain: </span><span class="text-amber-400 font-semibold">Claude Code + gstack</span>
</div>

---

# gstack: Roles, Not Prompts

<div class="mt-2 text-gray-300 text-sm mb-5">Each slash command is a distinct agentic role — and maps directly to GitHub's 5 patterns.</div>

<div class="space-y-3 text-sm">

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg border-l-4 border-amber-400">
  <div class="font-mono text-amber-400 w-44 shrink-0">/office-hours</div>
  <div class="w-32 shrink-0 text-gray-300">CEO / Product</div>
  <div class="text-gray-400 italic">Reactive Intelligence — validates the concept, pushes back on bad ideas</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg border-l-4 border-blue-400">
  <div class="font-mono text-blue-400 w-44 shrink-0">/plan-eng-review</div>
  <div class="w-32 shrink-0 text-gray-300">Eng Manager</div>
  <div class="text-gray-400 italic">Insight & Governance — locks architecture, surfaces risks, writes the test plan</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg border-l-4 border-purple-400">
  <div class="font-mono text-purple-400 w-44 shrink-0">/plan-design-review</div>
  <div class="w-32 shrink-0 text-gray-300">Designer</div>
  <div class="text-gray-400 italic">Continuous Improvement — 7 passes, 0–10 rating, kills AI slop before it ships</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg border-l-4 border-green-400">
  <div class="font-mono text-green-400 w-44 shrink-0">/ship</div>
  <div class="w-32 shrink-0 text-gray-300">Release Engineer</div>
  <div class="text-gray-400 italic">Orchestration — PR created, Vercel deployed, done</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg border-l-4 border-gray-400">
  <div class="font-mono text-gray-300 w-44 shrink-0">/simplify</div>
  <div class="w-32 shrink-0 text-gray-300">Self-review</div>
  <div class="text-gray-400 italic">Continuous Improvement — Claude reviews its own output, cuts the bloat</div>
</div>

</div>

<div class="mt-5 text-center text-gray-400 text-sm italic"><span class="line-through text-red-500">Not</span> a chat. A workflow.</div>

---
layout: center
---

# Meet Fafnir

<div class="flex items-center gap-10 mt-6 max-w-3xl mx-auto">

<div class="shrink-0">
  <img src="https://cxnebula71201.connexure.co/dropshare/Screen-Capture-2026-04-07-13-36-44-20260407173649-cd0b6c.png" class="rounded-xl border border-amber-400/30 max-h-56 object-contain shadow-xl" />
</div>

<div class="text-left space-y-4">
  <div class="text-xl font-semibold">A legendary dragon in the status line.</div>
  <div class="text-gray-300">Fafnir is a Claude Code buddy — watching every tool call, keeping score.</div>
  <div class="font-mono text-sm bg-gray-800/80 rounded-lg p-3 border border-gray-700">
    Peak stat: <span class="text-amber-400">SNARK (100)</span><br>
    Dump stat: <span class="text-red-400">PATIENCE (45)</span>
  </div>
  <div class="text-gray-400 text-sm mt-1">Introduced <span class="text-amber-400">March 31</span> as an April Fools feature. Anthropic removed it. <span class="text-green-400">Open Source FTW</span> — I added him back.</div>
  <div class="text-gray-400 text-sm italic">He disagreed with the design doc. He was right.</div>
</div>

</div>

---
layout: two-cols
---

# The Problem We Solved

<div class="mt-4 space-y-4 text-lg">

🏟️ **FIFA World Cup 2026** comes to Atlanta

🚌 **MARTA** is the answer — but fans don't know how to use it

📍 **3 zones** · 8 matches · 1 stadium

❓ *"How do I get to the game from where I am right now?"*

</div>

<div class="mt-6 text-gray-400 text-sm">
  Real question. Real fans. Real transit data.<br>
  The kind of problem you actually ship for.
</div>

::right::

<div class="mt-8 ml-8 p-6 bg-gray-800/80 rounded-xl border border-amber-400/30">

**Mercedes-Benz Stadium**
<div class="text-gray-400 text-sm mt-1">33.7545° N, 84.4025° W</div>

<div class="mt-4 space-y-2 text-sm">
  <div class="flex gap-2"><span class="text-amber-400">●</span> Gold Line → Five Points → stadium</div>
  <div class="flex gap-2"><span class="text-blue-400">●</span> Blue Line → Five Points → stadium</div>
  <div class="flex gap-2"><span class="text-orange-400">●</span> College Park → direct, ~30 min</div>
  <div class="flex gap-2"><span class="text-green-400">●</span> Bus routes 3, 21, 51</div>
</div>

</div>

---
layout: center
background: '#161b22'
---

# The Stack

<div class="grid grid-cols-2 gap-8 mt-8 text-left max-w-2xl mx-auto">

<div class="space-y-3">
  <div class="text-amber-400 font-semibold text-sm uppercase tracking-wider">Frontend</div>
  <div class="space-y-2 text-sm">
    <div>⬛ Next.js 16.2.2 (App Router)</div>
    <div>🎨 Tailwind 4 · shadcn/ui</div>
    <div>🗺️ Google Maps JS API (full-screen)</div>
    <div>📦 bun (not npm)</div>
  </div>
</div>

<div class="space-y-3">
  <div class="text-amber-400 font-semibold text-sm uppercase tracking-wider">Backend + AI</div>
  <div class="space-y-2 text-sm">
    <div>🤖 Claude (claude-sonnet-4-6)</div>
    <div>⚡ Vercel AI SDK v6 · streamText</div>
    <div>🚌 MARTA GTFS-RT + REST API</div>
    <div>🚀 Vercel (auto-deploy on push)</div>
  </div>
</div>

</div>

---
layout: center
---

# The Build in Numbers

<div class="mt-6 grid grid-cols-2 gap-6 max-w-2xl mx-auto">

<div class="p-5 bg-gray-800/80 rounded-xl border border-amber-400/30 text-center">
  <div class="text-4xl font-bold text-amber-400">13</div>
  <div class="font-semibold mt-1">issues found by /plan-eng-review</div>
  <div class="text-gray-300 text-xs mt-1">1 critical gap — Zod match schema — caught before a line was written</div>
</div>

<div class="p-5 bg-gray-800/80 rounded-xl border border-purple-400/30 text-center">
  <div class="text-4xl font-bold text-purple-400">4/10 → 8.5/10</div>
  <div class="font-semibold mt-1">design score after /plan-design-review</div>
  <div class="text-gray-300 text-xs mt-1">7 passes · full color palette written · under 10 minutes</div>
</div>

<div class="p-5 bg-gray-800/80 rounded-xl border border-green-400/30 text-center">
  <div class="text-4xl font-bold text-green-400">34s</div>
  <div class="font-semibold mt-1">git push → Vercel live</div>
  <div class="text-gray-300 text-xs mt-1">/ship handles the PR and deploy in one command</div>
</div>

<div class="p-5 bg-gray-800/80 rounded-xl border border-blue-400/30 text-center">
  <div class="text-4xl font-bold text-blue-400">~2h</div>
  <div class="font-semibold mt-1">bun create next-app → live on Vercel</div>
  <div class="text-gray-300 text-xs mt-1">Zero prior MARTA API experience going in</div>
</div>

</div>

<div class="mt-4 grid grid-cols-2 gap-4 max-w-2xl mx-auto">
  <img src="https://cxnebula71201.connexure.co/dropshare/Screen-Capture-2026-04-07-13-37-50-20260407173756-b5a78e.png" class="rounded-lg border border-gray-700 object-contain shadow-lg max-h-28 mx-auto" />
  <img src="https://cxnebula71201.connexure.co/dropshare/Screen-Capture-2026-04-07-13-58-02-20260407175809-af143b.png" class="rounded-lg border border-purple-400/40 object-contain shadow-lg max-h-28 mx-auto" />
</div>

---
layout: statement
---

# "Wait — the map IS the point."

<div class="text-xl mt-6 text-gray-300 max-w-xl mx-auto">
The design doc said no maps.<br>
<span class="text-amber-400">The user said the map was the whole demo.</span><br>
We pivoted. The map went in. Live MARTA data. Buses moving.
</div>

<div class="mt-8">
  <img src="https://cxnebula71201.connexure.co/dropshare/Screen-Capture-2026-04-07-15-01-00-20260407190108-2bace0.png" class="rounded-xl border border-amber-400/30 mx-auto max-h-44 object-contain shadow-xl" />
</div>

<div class="mt-6 text-gray-400 text-sm italic">
This is what good agentic collaboration looks like — the human has context the AI doesn't.
</div>

---

# Three Decisions That Shaped the App

<div class="mt-6 space-y-5">

<div class="flex gap-6 items-start">
  <div class="text-amber-400 font-bold text-2xl w-8 shrink-0">1</div>
  <div>
    <div class="font-semibold">inject_delay via POST body, not URL param</div>
    <div class="text-gray-300 text-sm mt-1">Client reads <code>?inject_delay=gold_line</code>, forwards it in the API body. Clean separation. The URL triggers; the server routes. Demo mode is invisible to the audience.</div>
  </div>
</div>

<div class="flex gap-6 items-start">
  <div class="text-amber-400 font-bold text-2xl w-8 shrink-0">2</div>
  <div>
    <div class="font-semibold">No SWR polling — server fetches MARTA inline</div>
    <div class="text-gray-300 text-sm mt-1">Background polling is wasted work. MARTA data fetches when Claude needs it, not continuously. The map handles its own 10s poll for vehicle positions — separate concern.</div>
  </div>
</div>

<div class="flex gap-6 items-start">
  <div class="text-amber-400 font-bold text-2xl w-8 shrink-0">3</div>
  <div>
    <div class="font-semibold">8s AbortController → pre-baked fallback (not an error)</div>
    <div class="text-gray-300 text-sm mt-1">Conference wifi is hostile. If Claude doesn't respond in 8 seconds, a human-written fallback renders. The user never sees a spinner forever. Resilience is a feature.</div>
  </div>
</div>

</div>

---
layout: center
---

# The Friend Voice Prompt

<div class="mt-6 max-w-2xl mx-auto text-left">

```
System: You are a local Atlanta friend who knows MARTA well.
You help FIFA World Cup fans get to Mercedes-Benz Stadium.
You speak plainly, like someone texting a friend.
Never sound like a transit app.
Never say "Route A", "minutes saved", or "optimal path."
If MARTA is bad, say so and give the real workaround.
Max 3 sentences.

User: I'm in {zone}. The match ({team_a} vs {team_b}) kicks off
in {minutes} minutes. MARTA status: {status}. What should I do?
```

</div>

<div class="mt-6 p-4 bg-gray-800/80 rounded-lg border border-amber-400/30 max-w-2xl mx-auto text-sm text-gray-300 italic">
"You're golden — hop on the Gold Line at Five Points, it goes straight to Mercedes-Benz Stadium. Takes about 5 minutes. Get there early, the concourse fills up fast."
</div>

<div class="mt-3 text-center text-gray-500 text-xs">3 sentences · no jargon · sounds like a person · streamed live via Vercel AI SDK</div>

---
layout: center
background: '#0d1117'
---

# 🔴 LIVE BUILD

<div class="text-2xl mt-6 text-gray-300">
We're building the <span class="text-amber-400">MARTA Status Card</span> right now.
</div>

<div class="mt-8 space-y-3 text-left max-w-lg mx-auto text-sm text-gray-400">
  <div>1. <code class="text-amber-400">/effort high</code> — think harder before we write anything</div>
  <div>2. Scaffold the component live</div>
  <div>3. <code class="text-amber-400">/simplify</code> — Claude reviews its own work</div>
  <div>4. <code class="text-green-400">/ship</code> — PR + Vercel in one command</div>
</div>

<div class="mt-10 text-gray-500 text-sm">
  Watch what Claude cuts. That's the lesson.
</div>

---
layout: center
---

# The Reveal ⚽

<div class="mt-4 text-3xl font-mono text-amber-400">
atl-fifa-navigator-v2.vercel.app
</div>

<div class="mt-3 text-gray-300">
Scan the QR · Try it on your phone · Pick a zone, pick a match, ask Claude
</div>

<div class="mt-6">
  <img src="https://cxnebula71201.connexure.co/dropshare/Screen-Capture-2026-04-09-23-13-32-20260410031344-c4ff7f.png" class="rounded-xl border border-amber-400/30 mx-auto max-h-52 object-contain shadow-2xl" />
</div>

<div class="mt-4 grid grid-cols-3 gap-4 text-sm text-center max-w-lg mx-auto">
  <div class="p-3 bg-gray-800/80 rounded">
    <div class="text-amber-400 font-semibold">Live MARTA</div>
    <div class="text-gray-300 text-xs mt-1">Real buses + trains, 10s updates</div>
  </div>
  <div class="p-3 bg-gray-800/80 rounded">
    <div class="text-amber-400 font-semibold">Claude Routing</div>
    <div class="text-gray-300 text-xs mt-1">Streaming friend-voice advice</div>
  </div>
  <div class="p-3 bg-gray-800/80 rounded">
    <div class="text-amber-400 font-semibold">Demo Mode</div>
    <div class="text-gray-300 text-xs mt-1">?inject_delay=gold_line</div>
  </div>
</div>

---

# What This Maps To

<div class="mt-2 text-gray-300 text-sm mb-4">Everything we built. Mapped back to GitHub's 5 patterns.</div>

<div class="space-y-3 text-sm">

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-44 shrink-0">/office-hours</div>
  <div class="text-gray-300 flex-1">Validates the concept, surfaces gaps, pushes back before code is written</div>
  <div class="text-amber-400 font-semibold text-xs w-36 shrink-0 text-right">Reactive Intelligence</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-blue-400 font-mono w-44 shrink-0">/plan-eng-review</div>
  <div class="text-gray-300 flex-1">13 issues found, 1 critical, architecture locked before a line was written</div>
  <div class="text-blue-400 font-semibold text-xs w-36 shrink-0 text-right">Insight & Governance</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-purple-400 font-mono w-44 shrink-0">/plan-design-review</div>
  <div class="text-gray-300 flex-1">4/10 → 8.5/10 in under 10 minutes, 7 automated passes</div>
  <div class="text-purple-400 font-semibold text-xs w-36 shrink-0 text-right">Continuous Improvement</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-green-400 font-mono w-44 shrink-0">/ship</div>
  <div class="text-gray-300 flex-1">PR created, Vercel deployed, live in 34 seconds — one command</div>
  <div class="text-green-400 font-semibold text-xs w-36 shrink-0 text-right">Orchestration</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-gray-300 font-mono w-44 shrink-0">Fafnir + /simplify</div>
  <div class="text-gray-300 flex-1">Watched every tool call, reviewed generated output, cut the bloat</div>
  <div class="text-gray-400 font-semibold text-xs w-36 shrink-0 text-right">Continuous Improvement</div>
</div>

</div>

<div class="mt-4 text-center text-amber-400 text-sm font-semibold">The practitioner proves the platform vision.</div>

---
layout: center
background: '#0d1117'
---

# Get the Tools

<div class="mt-8 grid grid-cols-2 gap-8 max-w-2xl mx-auto text-left">

<div>
  <div class="text-amber-400 font-semibold mb-2">Claude Code</div>
  <div class="font-mono text-sm text-gray-400">claude.ai/code</div>
  <div class="text-xs text-gray-500 mt-1">The CLI we used today</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">gstack</div>
  <div class="font-mono text-sm text-gray-400">github.com/garrys-list/gstack</div>
  <div class="text-xs text-gray-500 mt-1">The slash commands · open source</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">This app</div>
  <div class="font-mono text-sm text-gray-400">github.com/doctor-ew/atlaiweek-fifa</div>
  <div class="text-xs text-gray-500 mt-1">Full source, open</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">GitHub Agentic Workflows</div>
  <div class="font-mono text-sm text-gray-400">aka.ms/githubcopilotdevdays</div>
  <div class="text-xs text-gray-500 mt-1">The platform — Technical Preview</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">Live demo</div>
  <div class="font-mono text-sm text-gray-400">atl-fifa-navigator-v2.vercel.app</div>
  <div class="text-xs text-gray-500 mt-1">Try it · share it</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">These slides</div>
  <div class="font-mono text-sm text-gray-400">@doctorew</div>
  <div class="text-xs text-gray-500 mt-1">Find me after · ask anything</div>
</div>

</div>

---
layout: end
---

# Ship it.
