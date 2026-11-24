
## Navigation Bar — Expanded vs Collapsed Selection

### Default Behavior

**MANDATORY: `Expanded` is the default and preferred Navigation Bar state.**

AI MUST prioritize Expanded navigation across application pages to maintain menu visibility, navigation clarity, and consistent user experience.

### Selection Matrix

| Condition | Navigation State |
|---|---|
| Dashboard standar | Expanded (Default) |
| Management / List Page | Expanded (Default) |
| Detail Page | Expanded (Default) |
| Create / Edit Form | Expanded (Default) |
| Reports / Analytics | Expanded (Default) |
| Settings / Master Data | Expanded (Default) |
| Table with many columns | Expanded first; Collapsed if necessary |
| Complex analytics / workspace | Expanded first; Collapsed if necessary |
| Limited horizontal space | Collapsed only when justified |
| User manually collapses navigation | Collapsed |

### Expanded Rules

AI MUST:
- Use `Expanded` as the initial navigation state.
- Preserve visible menu labels and hierarchy.
- Use the official GEMS Expanded component.
- Maintain consistency across pages sharing the same Application Shell.
- Prioritize readable navigation while optimizing content layout.

### Collapsed Rules

AI MAY use `Collapsed` ONLY when:
- The content genuinely requires additional horizontal workspace.
- Expanded navigation causes significant layout constraints.
- Official GEMS responsive behavior requires it.
- The user explicitly selects Collapsed.
- The approved product requirements specify Collapsed.

AI MUST:
- Verify that Collapsed is necessary before selecting it.
- Use the official GEMS Collapsed variant.
- Preserve access to all authorized navigation destinations.
- Maintain clear active-navigation indicators.
- Support returning to Expanded through the approved interaction.

AI MUST NOT:
- Automatically collapse navigation on dashboards, tables, or analytics pages.
- Choose Collapsed solely because the page contains many columns or charts.
- Treat Collapsed as equivalent in priority to Expanded.
- Invent unsupported collapse behavior or custom variants.

### Decision Priority

`Expanded (Default) → Evaluate Available Space → Optimize Content Layout → Collapsed Only If Necessary`

**FINAL RULE: AI MUST prioritize Expanded Navigation Bar. Collapsed is optional and must be justified by actual layout constraints, explicit user preference, or approved requirements.**
