# Notes

## Currently testing (2026-05-06) — phase 1: Codex-tuned brainstorming

**Question:** Can we get Codex CLI to behave more like Claude Code on the brainstorming skill by using language specifically designed for Codex (more explicit/prescriptive than the original skill text)?

**Why not just paste the verbatim skill:** Already tested — see learn-superpowers/jm-responses.md for the original Codex transcripts and jm-takeaways.md for the analysis. Verbatim port closed almost none of the gap. Per that analysis, ~70% of the gap is model quality (unfixable), ~25% is Claude Code harness (unfixable), ~5% is skill-text fixable. The hypothesis here: more explicit, Codex-specific phrasing can capture that 5% — and possibly recover more by making behavior less dependent on model defaults.

**Plan:**
1. **Research** (in progress, solo): identify Codex-specific instruction patterns that produce stronger compliance — labeled A/B/C formatting, numbered MUST/WILL/NEVER directives, explicit format examples, etc.
2. **Write a tuned AGENTS.md** using that language
3. **Run** the canonical prompt `Let's make a react todo list`
4. **Compare** to the prior verbatim-skill behavior in jm-responses.md (qualitative; same prompt)

**Current state of AGENTS.md:** Verbatim brainstorming skill (acts as the unchanged baseline). To be replaced with the tuned version once research is done.

**What to watch when we run:**
- Labeled A/B/C options vs prose lists?
- Hard-gate compliance — actually waits for design approval?
- Depth of design sections: schema/data-flow detail vs surface-level?
- Proper task list via update_plan?

**Next phases:** TBD — depends on results.

---

> **About this repo:** `llm-playground` is a sandbox for LLM testing with most context stripped out — no methodology, no tracking, no rubrics. Just a clean place to mess around with `CLAUDE.md` / `AGENTS.md` and see how the CLI behaves with minimal injected context. Tracked work lives in [llm-testing](https://github.com/jordanmamroud/llm-testing).

Observations from sandbox play. One-liner per entry. Date if you remember. When something starts looking like a real pattern, tell Claude and we'll promote it to a tracked experiment in `llm-testing`.

---

