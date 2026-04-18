# What This Maps To — Scale 1

<div class="mt-2 text-gray-300 text-sm mb-4">The scrappy build. GitHub tools, zero prior domain knowledge, ~2 hours.</div>

<div class="space-y-3 text-sm">

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-44 shrink-0">Copilot Chat</div>
  <div class="text-gray-300 flex-1">Validates approach, surfaces API questions, pushes back before code is written</div>
  <div class="text-amber-400 font-semibold text-xs w-36 shrink-0 text-right">Reactive Intelligence</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-blue-400 font-mono w-44 shrink-0">Copilot Code Review</div>
  <div class="text-gray-300 flex-1">Architecture feedback, critical gaps surfaced before merge</div>
  <div class="text-blue-400 font-semibold text-xs w-36 shrink-0 text-right">Insight & Governance</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-purple-400 font-mono w-44 shrink-0">Vercel preview deploys</div>
  <div class="text-gray-300 flex-1">Every push gets a preview URL — feedback loop tightens to seconds</div>
  <div class="text-purple-400 font-semibold text-xs w-36 shrink-0 text-right">Continuous Improvement</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-green-400 font-mono w-44 shrink-0">gh pr create + deploy</div>
  <div class="text-gray-300 flex-1">PR → Vercel → live in 34 seconds — the whole loop automated</div>
  <div class="text-green-400 font-semibold text-xs w-36 shrink-0 text-right">Orchestration</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-gray-300 font-mono w-44 shrink-0">Human pivot</div>
  <div class="text-gray-300 flex-1">"The map IS the point" — user context the AI didn't have. Engineer decides.</div>
  <div class="text-gray-400 font-semibold text-xs w-36 shrink-0 text-right">The irreducible human</div>
</div>

</div>

<div class="mt-4 text-center text-amber-400 text-sm font-semibold">The practitioner proves the platform vision.</div>

---

# What This Maps To — Scale 2

<div class="mt-2 text-gray-300 text-sm mb-4">The production pipeline. Same 5 patterns, enterprise stakes.</div>

<div class="space-y-3 text-sm">

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-44 shrink-0">/spec + code-fact-extractor</div>
  <div class="text-gray-300 flex-1">Every identifier verified before the spec is written — adversarial gate at the task layer</div>
  <div class="text-blue-400 font-semibold text-xs w-36 shrink-0 text-right">Insight & Governance</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-blue-400 font-mono w-44 shrink-0">/review-spec</div>
  <div class="text-gray-300 flex-1">QA validates task ↔ spec ↔ code alignment — catches drift before the PR opens</div>
  <div class="text-blue-400 font-semibold text-xs w-36 shrink-0 text-right">Insight & Governance</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-amber-400 font-mono w-44 shrink-0">/review</div>
  <div class="text-gray-300 flex-1">Code reviewer reacts to every change; security auditor fires automatically on auth</div>
  <div class="text-amber-400 font-semibold text-xs w-36 shrink-0 text-right">Reactive Intelligence</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-green-400 font-mono w-44 shrink-0">/preflight</div>
  <div class="text-gray-300 flex-1">Deploy interview + script validation — manifest generated, nothing ships without it</div>
  <div class="text-green-400 font-semibold text-xs w-36 shrink-0 text-right">Orchestration</div>
</div>

<div class="flex items-start gap-4 p-3 bg-gray-800/80 rounded-lg">
  <div class="text-purple-400 font-mono w-44 shrink-0">scope-detection hook</div>
  <div class="text-gray-300 flex-1">Fires on every edit — alerts when session has grown beyond single-agent scope</div>
  <div class="text-purple-400 font-semibold text-xs w-36 shrink-0 text-right">Continuous Improvement</div>
</div>

</div>

<div class="mt-4 text-center text-amber-400 text-sm font-semibold">Two scales. Same platform vision. The practitioner proves both.</div>

---
layout: center
background: '#0d1117'
---

# Get the Tools

<div class="mt-8 grid grid-cols-2 gap-8 max-w-2xl mx-auto text-left">

<div>
  <div class="text-amber-400 font-semibold mb-2">GitHub Copilot</div>
  <div class="font-mono text-sm text-gray-400">github.com/features/copilot</div>
  <div class="text-xs text-gray-500 mt-1">The AI we used today</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">GitHub Agentic Workflows</div>
  <div class="font-mono text-sm text-gray-400">aka.ms/githubcopilotdevdays</div>
  <div class="text-xs text-gray-500 mt-1">The platform — Technical Preview</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">This app</div>
  <div class="font-mono text-sm text-gray-400">github.com/doctor-ew/atlaiweek-fifa</div>
  <div class="text-xs text-gray-500 mt-1">Full source, open</div>
</div>

<div>
  <div class="text-amber-400 font-semibold mb-2">gh aw CLI</div>
  <div class="font-mono text-sm text-gray-400">gh extension install github/gh-aw</div>
  <div class="text-xs text-gray-500 mt-1">Run the live demo yourself</div>
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
