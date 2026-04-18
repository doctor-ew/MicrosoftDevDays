---
layout: statement
---

# Two Scales, One Pattern

<div class="mt-10 grid grid-cols-2 gap-12 max-w-2xl mx-auto text-left">

<div class="space-y-3 p-5 bg-gray-800/80 rounded-xl border border-amber-400/30">
  <div class="text-amber-400 font-semibold text-sm uppercase tracking-wider">Scale 1 — Scrappy</div>
  <div class="text-3xl font-bold">~2h</div>
  <div class="text-gray-300 text-sm">1 developer · new API · zero prior domain knowledge · live on Vercel</div>
</div>

<div class="space-y-3 p-5 bg-gray-800/80 rounded-xl border border-blue-400/30">
  <div class="text-blue-400 font-semibold text-sm uppercase tracking-wider">Scale 2 — Production</div>
  <div class="text-3xl font-bold">spec → ship</div>
  <div class="text-gray-300 text-sm">Adversarial verification · 3-doc QA · nothing merges without a preflight</div>
</div>

</div>

<div class="mt-10 text-center text-gray-400 text-lg">Same underlying pattern. Different stakes.</div>

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
    <div>🤖 GitHub Copilot · streaming advice</div>
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
  <div class="text-4xl font-bold text-amber-400">~2h</div>
  <div class="font-semibold mt-1">zero → live on Vercel</div>
  <div class="text-gray-300 text-xs mt-1">Zero prior MARTA API experience going in</div>
</div>

<div class="p-5 bg-gray-800/80 rounded-xl border border-blue-400/30 text-center">
  <div class="text-4xl font-bold text-blue-400">34s</div>
  <div class="font-semibold mt-1">git push → Vercel live</div>
  <div class="text-gray-300 text-xs mt-1">PR created, preview deployed, production promoted</div>
</div>

<div class="p-5 bg-gray-800/80 rounded-xl border border-green-400/30 text-center">
  <div class="text-4xl font-bold text-green-400">3</div>
  <div class="font-semibold mt-1">MARTA data sources integrated</div>
  <div class="text-gray-300 text-xs mt-1">GTFS-RT vehicle positions · alerts · trip updates</div>
</div>

<div class="p-5 bg-gray-800/80 rounded-xl border border-purple-400/30 text-center">
  <div class="text-4xl font-bold text-purple-400">1 pivot</div>
  <div class="font-semibold mt-1">design doc said no maps</div>
  <div class="text-gray-300 text-xs mt-1">User said the map was the whole demo. Human wins.</div>
</div>

</div>

<div class="mt-4 text-center">
  <img src="https://cxnebula71201.connexure.co/dropshare/Screen-Capture-2026-04-07-15-01-00-20260407190108-2bace0.png" class="rounded-lg border border-amber-400/30 object-contain shadow-lg max-h-28 mx-auto" />
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
