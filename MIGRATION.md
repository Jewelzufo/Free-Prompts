# Migration

How the November 2026 reorganization moved every file from the year-first tree to the use-case-first tree. Every move used `git mv`, so history is preserved.

## Path map

| Old path | New path |
| --- | --- |
| `2025-Catalog/2025 templates 1` | `prompts/general/100-prompt-basics.md` |
| `2025-Catalog/20_LLM_Prompts.md` | `prompts/general/20-productivity-prompts.md` |
| `2025-Catalog/10-novel-templates.md` | `prompts/general/10-novel-templates.md` |
| `2025-Catalog/10-advanced-reasoning-templates.txt` | `prompts/general/10-advanced-reasoning-templates.md` |
| `2025-Catalog/Prompts-ai-engineering.md` | `prompts/general/ai-engineering-prompts.md` |
| `2025-Catalog/10-Data-analysis-prompts.md` | `prompts/data-analysis/10-data-analysis-prompts.md` |
| `2025-Catalog/data-prompts.md` | `prompts/data-analysis/20-structured-prompts.md` |
| `2025-Catalog/analysis templates` | `prompts/data-analysis/data-analysis-templates.md` |
| `2025-Catalog/Data Analyst Prompts` | `prompts/data-analysis/data-analyst-prompts.md` |
| `2026-Catalog/General/MKT_Prompts.md` | `prompts/marketing/marketing-prompts.md` |
| `2025-Catalog/enterprise/enterprise.md` | `prompts/enterprise/ibm-granite-enterprise-prompts.md` |
| `2025-Catalog/enterprise/enterprise-templates.md` | `prompts/enterprise/enterprise-content-templates.md` |
| `2026-Catalog/General/Advanced_Techniques_2026.md` | `prompts/enterprise/enterprise-prompt-templates-2026.md` |
| `2025-Catalog/Manus Prompt Template_ Code Debugging, Testing, and Refactoring.md` | `prompts/coding/manus-code-debugging-testing-refactoring.md` |
| `2026-Catalog/system-prompts/nl_to_python.md` | `prompts/coding/nl-to-python-system-prompt.md` |
| `2026-Catalog/General/universal_template.md` | `templates/universal-template.md` |
| `2026-Catalog/langchain-prompts/universal_template_01.md` | `templates/universal-template-langchain.md` |
| `2025-Catalog/multilayer_template` | `templates/multilayer-template.md` |
| `2025-Catalog/one page website template` | `templates/one-page-website-template.md` |
| `2026-Catalog/Structured/XML/claude_template.md` | `templates/xml/claude-universal-xml-template.md` |
| `2026-Catalog/Structured/XML/general_prompt-template.md` | `templates/xml/general-xml-template.md` |
| `Prompt-Guides/gpt5-prompting.md` | `guides/gpt-5-prompting.md` |
| `2026-Catalog/gpt_54_prompt.md` | `guides/gpt-5-4-universal-prompt.md` |
| `2026-Catalog/General/deepseek_2026.md` | `guides/deepseek-prompting-2026.md` |
| `Prompt-Guides/ibm_prompt_guide_2026.md` | `guides/ibm-prompt-engineering-guide-2026.md` |
| `2025-Catalog/llm_prompting_formats.md` | `guides/llm-prompting-formats.md` |
| `techniques/prompt-techniques.md` | `techniques/50-prompt-techniques.md` |
| `techniques/prompting_simplified.md` | `techniques/prompting-simplified.md` |
| `2026-Catalog/agent-fleets/fleet1.md` | `agents/agent-fleets.md` |
| `2026-Catalog/Orchestration/Master-Orchestrator-U.md` | `agents/master-orchestrator-u.md` |
| `2026-Catalog/Orchestration/Orchestrator-Omni.md` | `agents/orchestrator-omni.md` |
| `2026-Catalog/General/self_improving_AGENTS.md` | `agents/self-improving-agents.md` |
| `2026-Catalog/General/q_learning_simulator.md` | `agents/q-learning-simulator.md` |
| `2026-Catalog/General/meta_q_learning_sim.md` | `agents/q-learning-simulation.md` |
| `2026-Catalog/General/nlp_pos_tagging.md` | `agents/nlp-pos-tagging.md` |
| `2025-Catalog/prompt-arsenal-01/Prompt_Arsenal_1.md` | `packs/prompt-arsenal-01.md` |
| `assets/Prompt Arsenal-01.png` | `assets/Prompt Arsenal-01.png` (kept, see note below) |
| `assets/ChatGPT Image Jun 3, 2025, 08_29_43 PM.png` | `assets/ChatGPT Image Jun 3, 2025, 08_29_43 PM.png` (kept, see note below) |

## Deleted files

Three files were deleted, each by a written decision. All three are recoverable from git history.

- `2026-Catalog/meta-prompts/q_learning_sim.md`: Formatting-only duplicate of 2026-Catalog/General/meta_q_learning_sim.md: diff is '**Prompt:**' vs 'Prompt:' plus an outer code fence. No unique content.
- `2025-Catalog/2025 Templates 2`: Exact duplicate subset: items 21-100 are byte-identical to items 21-100 of '2025 templates 1' (80 of 80 identical). No unique content; the merged file is '2025 templates 1' verbatim.
- `2026-Catalog/General/DA_Prompts.md`: 4-byte stub containing only 'init', created that way in f38e80c. Never held real content; nothing to restore.

## Deviations from the November 10 proposal

- `prompts/data-analysis/` holds four files, not three. `data-prompts.md` became `20-structured-prompts.md`, not `structured-data-prompts.md`, because its 20 templates span legal, research, PR, technical, and creative domains, not data analysis alone. The fourth file is `data-analyst-prompts.md`, the reformatted single-line file.
- `prompts/enterprise/enterprise-prompt-templates-2026.md` keeps its existing frontmatter `description` and adds the common `category`, `models`, `use_case`, and `updated` fields.
- New files not in the proposal tree: this file, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, and two issue templates. The proposal called for the community files; this file records the mapping and the deletion decisions.
- The two PNGs keep their original filenames. The local reorg commit renamed them to kebab-case, but the push went through the GitHub connector, which cannot upload binary files, so the renames were reverted before pushing and the two image links point at the original names. The kebab-case names are preserved in the local bundle for the reorg commit if they are wanted later.

## Verification

Checked after the move, all passed on 2026-11-11:

- Mapping: all 44 old files account for exactly one new path, one of the three deletion decisions, or the two files kept in place (root README, LICENSE). No old year directories remain.
- Content: every moved file is byte-identical apart from its added frontmatter, except the five fixed files listed above, each verified by diff. Both PNGs are byte-identical.
- Links: every relative link and image in every Markdown file resolves. No absolute github.com blob link to a repo file remains.
- Catalog: CATALOG.md lists all 37 content files once, matching the tree. Root README counts match the tree.
- Frontmatter: all 37 content files carry title, category, models, use_case, and updated.
- No extensionless files remain, and no two content files are byte-identical.
