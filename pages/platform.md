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
