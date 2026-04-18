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
  <span class="text-gray-300">The practitioner's answer: </span><span class="text-amber-400 font-semibold">a spec-driven workflow</span>
</div>

---
layout: center
---

# The 5 Domains — What Practitioners Actually Need

<div class="text-gray-400 text-sm text-center mb-6">Provider-agnostic. These apply whether you're using Copilot, Claude, or Cursor.</div>

<div class="grid grid-cols-5 gap-2 max-w-4xl mx-auto text-xs">

<div class="p-3 bg-gray-800/80 rounded-xl border border-amber-400/40 flex flex-col">
  <div class="text-amber-400 font-bold text-lg">27%</div>
  <div class="text-gray-500 text-xs mb-1">Domain 1</div>
  <div class="font-semibold text-sm mb-2">Agentic Architecture & Orchestration</div>
  <div class="text-gray-400 text-xs flex-1">Hub-and-spoke patterns, context isolation, task decomposition, forking, loop enforcement</div>
  <div class="mt-2 text-amber-500 text-xs italic">Trap: using few-shot examples to enforce tool ordering</div>
</div>

<div class="p-3 bg-gray-800/80 rounded-xl border border-blue-400/40 flex flex-col">
  <div class="text-blue-400 font-bold text-lg">18%</div>
  <div class="text-gray-500 text-xs mb-1">Domain 2</div>
  <div class="font-semibold text-sm mb-2">Tool Design & MCP Integration</div>
  <div class="text-gray-400 text-xs flex-1">Tool interface descriptions, structured error responses, scoping tools to specific agent roles</div>
  <div class="mt-2 text-amber-500 text-xs italic">Trap: returning empty results on subagent failure</div>
</div>

<div class="p-3 bg-gray-800/80 rounded-xl border border-purple-400/40 flex flex-col">
  <div class="text-purple-400 font-bold text-lg">20%</div>
  <div class="text-gray-500 text-xs mb-1">Domain 3</div>
  <div class="font-semibold text-sm mb-2">AI Dev Tool Config & Workflows</div>
  <div class="text-gray-400 text-xs flex-1">Instruction hierarchies, rule propagation, custom commands, plan mode vs. direct execution</div>
  <div class="mt-2 text-amber-500 text-xs italic">Trap: assuming larger context fixes attention dilution</div>
</div>

<div class="p-3 bg-gray-800/80 rounded-xl border border-green-400/40 flex flex-col">
  <div class="text-green-400 font-bold text-lg">20%</div>
  <div class="text-gray-500 text-xs mb-1">Domain 4</div>
  <div class="font-semibold text-sm mb-2">Prompt Engineering & Structured Output</div>
  <div class="text-gray-400 text-xs flex-1">JSON schema design, few-shot selection, validation loops, output contract design at scale</div>
  <div class="mt-2 text-amber-500 text-xs italic">Trap: self-reported confidence scores for routing</div>
</div>

<div class="p-3 bg-gray-800/80 rounded-xl border border-red-400/40 flex flex-col">
  <div class="text-red-400 font-bold text-lg">15%</div>
  <div class="text-gray-500 text-xs mb-1">Domain 5</div>
  <div class="font-semibold text-sm mb-2">Context Management & Reliability</div>
  <div class="text-gray-400 text-xs flex-1">Preserving context across long interactions, escalation patterns, silent failure prevention</div>
  <div class="mt-2 text-amber-500 text-xs italic">Trap: routing all workflows to Batch API for cost savings</div>
</div>

</div>

<div class="mt-5 text-center text-gray-500 text-xs">Like the AWS Well-Architected Framework — the discipline doesn't change just because the tool does.</div>
