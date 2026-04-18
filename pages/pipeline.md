---
layout: statement
---

# The Spec Is the Contract

<div class="mt-10 grid grid-cols-2 gap-12 max-w-2xl mx-auto text-left">

<div class="space-y-3">
  <div class="text-amber-400 font-semibold text-sm uppercase tracking-wider">The problem</div>
  <div class="text-lg">AI makes building fast. It doesn't make building the <em>right thing</em> easier.</div>
  <div class="text-gray-300 text-sm">Without a spec, the engineer and the AI are both guessing about intent.</div>
</div>

<div class="space-y-3">
  <div class="text-amber-400 font-semibold text-sm uppercase tracking-wider">The rule</div>
  <div class="text-lg font-semibold">No code without a spec.</div>
  <div class="text-gray-300 text-sm">The spec is not a planning doc. It's the contract between the ticket and the implementation.</div>
</div>

</div>

<div class="mt-12 text-center text-gray-400 italic text-lg max-w-xl mx-auto">
  "If you can't write it down, you're not ready to build it."
</div>

---
layout: center
---

# The Pipeline — Handoff Gates

<div class="mt-4 max-w-2xl mx-auto space-y-2 text-sm">

<div class="flex items-center gap-3 p-3 bg-gray-800/80 rounded-lg">
  <div class="font-mono text-amber-400 w-32 shrink-0">/spec</div>
  <div class="flex-1 text-gray-300">Spec Writer agent — task → spec with verified, cited sources</div>
  <div class="text-amber-400 text-xs border border-amber-400/40 rounded px-2 py-0.5 shrink-0">ENGINEER APPROVES</div>
</div>

<div class="text-center text-gray-600">↓</div>

<div class="flex items-center gap-3 p-3 bg-gray-800/80 rounded-lg">
  <div class="font-mono text-blue-400 w-32 shrink-0">/implement</div>
  <div class="flex-1 text-gray-300">Engineer or Architect agent — scope-routed automatically</div>
  <div class="text-green-400 text-xs border border-green-400/40 rounded px-2 py-0.5 shrink-0">TESTS GREEN</div>
</div>

<div class="text-center text-gray-600">↓</div>

<div class="flex items-center gap-3 p-3 bg-gray-800/80 rounded-lg">
  <div class="font-mono text-purple-400 w-32 shrink-0">/review-spec</div>
  <div class="flex-1 text-gray-300">QA agent — 3-doc check: task ↔ spec ↔ code. Flags drift before PR opens.</div>
  <div class="text-purple-400 text-xs border border-purple-400/40 rounded px-2 py-0.5 shrink-0">ALIGNED</div>
</div>

<div class="text-center text-gray-600">↓</div>

<div class="flex items-center gap-3 p-3 bg-gray-800/80 rounded-lg">
  <div class="font-mono text-orange-400 w-32 shrink-0">/review</div>
  <div class="flex-1 text-gray-300">Code Reviewer + Security Auditor — parallel on auth/secrets changes</div>
  <div class="text-orange-400 text-xs border border-orange-400/40 rounded px-2 py-0.5 shrink-0">QUALITY</div>
</div>

<div class="text-center text-gray-600">↓</div>

<div class="flex items-center gap-3 p-3 bg-gray-800/80 rounded-lg">
  <div class="font-mono text-green-400 w-32 shrink-0">/preflight</div>
  <div class="flex-1 text-gray-300">7-question deploy interview + script validation → deployment manifest</div>
  <div class="text-green-400 text-xs border border-green-400/40 rounded px-2 py-0.5 shrink-0">DEPLOY SAFE</div>
</div>

</div>

<div class="mt-4 text-center text-gray-500 text-xs">Agents propose. Engineers decide. Every gate is a human handoff.</div>

---
layout: two-cols
---

# The Adversarial Gate

<div class="mt-4 space-y-4 text-sm">

<div class="p-4 bg-gray-800/80 rounded-lg border-l-4 border-red-400">
  <div class="font-semibold text-red-400 mb-2">The failure mode</div>
  <div class="text-gray-300">The spec says <code>getActiveRoutes()</code> exists. It doesn't. Engineer implements against a ghost. Three days of rework.</div>
</div>

<div class="p-4 bg-gray-800/80 rounded-lg border-l-4 border-amber-400">
  <div class="font-semibold text-amber-400 mb-2">The fix</div>
  <div class="text-gray-300">Before a single line is written into the spec, the <code>code-fact-extractor</code> agent verifies every identifier against the actual codebase.</div>
</div>

<div class="p-4 bg-gray-800/80 rounded-lg border-l-4 border-green-400">
  <div class="font-semibold text-green-400 mb-2">The rule</div>
  <div class="text-gray-300 font-semibold">Absence of evidence = absence from the spec.</div>
  <div class="text-gray-400 text-xs mt-1">If it isn't found, it doesn't go in. Block until the engineer confirms. No substitutions.</div>
</div>

</div>

::right::

<div class="ml-6 mt-4 space-y-4 text-sm">

<div class="p-4 bg-gray-800/80 rounded-lg border border-gray-700">
  <div class="font-semibold text-gray-300 mb-2">Works Cited — mandatory section</div>
  <div class="font-mono text-xs text-gray-400 space-y-1">
    <div><span class="text-green-400">✅ VERIFIED</span></div>
    <div class="pl-2 text-gray-500">src/services/marta.ts:88-104</div>
    <div class="pl-2 text-gray-500">(branch: main, commit: c7d2f1)</div>
    <div class="pl-2 text-gray-500">— confirms getActiveRoutes signature</div>
    <div class="mt-2"><span class="text-red-400">❌ NOT FOUND</span></div>
    <div class="pl-2 text-gray-500">getRealTimeETA — not in codebase.</div>
    <div class="pl-2 text-gray-500">Do not include. Ask engineer first.</div>
  </div>
</div>

<div class="text-gray-400 text-xs mt-2 italic">
  GitHub's "threat detection scans output before execution" — applied at the spec layer, before execution begins.
</div>

<div class="mt-4 p-3 bg-amber-400/10 rounded-lg border border-amber-400/30 text-xs text-gray-300">
  Every method name, file path, return code, and field name in the spec is cited by file, line range, branch, and commit SHA.
</div>

</div>
