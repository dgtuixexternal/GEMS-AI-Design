
# GEMS Design System — Design Annotations

> **CONDITIONAL:** Use official GEMS Design Annotations only for UI/UX documentation, interaction explanations, design specifications, and developer handoff. Annotations are not production UI elements.

## 1. Sources & Priority

**Source of Truth**
- [GEMS Design Annotations](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=378-12201)
- Relevant GEMS Components, Page Samples & UX Patterns within the same Figma Design System.

**Priority Order**
1. **Official Components:** Use existing GEMS Design Annotation components and variants.
2. **Documentation Context:** Select annotations based on the information that needs explanation.
3. **GEMS Examples:** Read relevant examples for actual annotation usage and placement.

Read only references relevant to the current task.

## 2. Available Annotation Components

| Component | Usage |
|---|---|
| Design Note | Explain design decisions, behavior, and implementation notes |
| Measure + Spacing Guide | Document dimensions, spacing, and layout measurements |
| Measure Line | Indicate measured distances or spacing |
| Cursor | Illustrate user interactions |
| Keyboard Key | Display individual keyboard shortcuts |
| Key Combination | Display combinations of keyboard shortcuts |
| Documentation Table Cell | Structure component or specification documentation |
| Design System Header | Organize design-system documentation |

Use official variants, sizes, and properties defined in GEMS Figma.

## 3. Context-Based Annotation Usage

AI MUST determine whether annotations are necessary based on the task.

**Use Annotations When**
- Creating UI/UX documentation or specifications.
- Explaining complex component behavior.
- Documenting interaction flows and state transitions.
- Preparing developer handoff.
- Explaining responsive layout behavior.
- Documenting keyboard shortcuts or accessibility interactions.
- Clarifying measurements or implementation requirements.

**Do NOT Use Annotations When**
- Creating standard production UI screens.
- Designing dashboards, forms, tables, or cards without documentation requirements.
- Building user-facing application layouts.
- Adding decorative or unnecessary explanations.

**Rules**
- Use only annotations relevant to the design or handoff.
- Keep annotations separate from production UI.
- Position annotations without obscuring important interface elements.
- Use concise and accurate descriptions.
- Explain actual approved behavior, not assumptions.
- Avoid duplicating information already clearly represented in the design.
- Do not annotate every component automatically.

## 4. Component Application Rules

**Design Notes**
- Use for important design decisions, interaction behavior, or implementation requirements.
- Follow official GEMS Size variants.
- Keep descriptions concise and implementation-focused.

**Measurement Guides**
- Use for dimensions, padding, gaps, and alignment when explicit measurements are needed.
- Follow official GEMS measurement components and variants.
- Use actual design measurements; do not invent dimensions.

**Cursor & Keyboard Keys**
- Use to demonstrate supported interactions and keyboard shortcuts.
- Follow official Cursor states and Keyboard Key variants.
- Do not document shortcuts that are not implemented or approved.

**Documentation Tables**
- Use for structured component specifications and design documentation.
- Follow official GEMS table-cell variants.
- Do not replace production Data Table components with documentation tables.

**Design System Headers**
- Use for design-system documentation sections.
- Do not use as application Page Headers.

## 5. Strict Annotation Rules

**MUST**
- Use official GEMS Design Annotation components.
- Select annotations according to documentation needs.
- Preserve original component variants and visual properties.
- Maintain clear separation between documentation and production UI.
- Document accurate behavior, measurements, and specifications.
- Read relevant GEMS examples when necessary.

**MUST NOT**
- Add annotations automatically to every UI screen.
- Treat annotations as user-facing application components.
- Create custom annotation styles when official GEMS components exist.
- Invent interaction behavior, measurements, or technical specifications.
- Add unnecessary or repetitive documentation.
- Modify official typography, colors, spacing, or component properties.
- Use Design System Headers as production Page Headers.

**Fallback:** If the task does not require documentation, specifications, or developer handoff, do not use Design Annotations.

**Core Principle:** Design Annotations explain the design. They must improve communication and implementation clarity without becoming part of the production interface.
