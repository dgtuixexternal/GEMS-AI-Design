
# GEMS Design System — Foundation / Icons

> **MANDATORY:** All UI icons MUST use official GEMS Figma Icon Components. Line/Outline Icons are the default. Icon selection, size, style, and placement MUST follow official component specifications and product context.

## 1. Sources & Priority

**Source of Truth**
- [GEMS Icons](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-1131)
- GEMS Components, Page Samples & UX Pattern Samples within the same Figma Design System.

**Priority Order**
1. **Component Icons:** Use icons already defined within official GEMS Components.
2. **GEMS Icon Library:** Select existing official icons when a component or feature requires an icon.
3. **Page Samples & UX Patterns:** Read relevant examples for actual icon usage, size, placement, and visual consistency.
4. **General UX Principles:** Apply only when GEMS has no specific guidance.

Read only references relevant to the current task. Do not scan unrelated pages or components.

Official GEMS Component specifications always take priority.

## 2. Icon Style & Visual Rules

**Default Style: Line / Outline Icons**

- MUST prioritize official GEMS Line/Outline Icons.
- Filled Icons are allowed only when specified by official GEMS Components, variants, or approved designs.
- Preserve original icon proportions, stroke, fill, and visual properties.
- Maintain consistent icon style across related UI elements.
- Do not mix Line and Filled Icons arbitrarily.
- Do not convert icons manually between Line and Filled styles.
- Do not replace official icons based on visual preference.

**Icon Colors**
- Use official GEMS Color tokens.
- Follow semantic foreground and interaction state colors.
- Preserve colors defined by official component variants.
- Do not manually recolor icons outside GEMS token specifications.

## 3. Icon Size & Placement

Icon sizing MUST follow official GEMS Component specifications.

**Size Priority**
1. Use the icon size defined by the parent GEMS Component.
2. Use the available official icon size or variant when applicable.
3. Refer to relevant Page Samples and UX Patterns for contextual sizing.

**Rules**
- Preserve original icon aspect ratio and proportions.
- Follow component-specific icon size, padding, gap, and alignment.
- Maintain consistent sizing for identical icon functions.
- Do not manually enlarge or shrink icons outside official specifications.
- Do not use arbitrary icon sizes or custom scaling.
- Do not adjust icon stroke width to compensate for size changes.
- Do not change icon positioning independently from the parent component.

## 4. Component Icon Integration

Icons MUST remain consistent with official GEMS Components.

**Component Usage**

| Component | Icon Rules |
|---|---|
| Button | Use official leading/trailing icons and supported variants |
| Input | Follow official prefix/suffix icon specifications |
| Dropdown | Preserve official chevron and indicator icons |
| Navigation | Follow official menu icons and active states |
| Table | Use official action icons and Table patterns |
| Alert & Notification | Use appropriate semantic status icons |
| Modal | Use official close and supporting icons |
| Tabs | Use icons only when supported by official variants |
| Empty State | Follow GEMS Empty State icon specifications |
| Featured Icon | Use official GEMS Featured Icon components |

**Rules**
- Preserve existing component icons and their properties.
- Use official icon visibility or instance-swap properties when available.
- Do not detach or manually recreate icon components.
- Do not insert extra icons into components unless supported by their official variants.
- Use consistent icon mapping for identical actions across pages.
- Follow official component interaction states.

## 5. Featured Icon Usage

Featured Icons MUST use official GEMS Featured Icon components.

**Rules**
- Use Featured Icon components for prominent visual indicators when required by GEMS.
- Follow official Featured Icon sizes, variants, colors, radius, and backgrounds.
- Refer to relevant Page Samples and UX Patterns for appropriate usage.
- Do not create Featured Icons by enlarging regular icons.
- Do not manually add decorative backgrounds, circles, or containers to regular icons.
- Do not invent Featured Icon variants or visual treatments.
- Do not use Featured Icons automatically for every Card, Section, or Empty State.

**Core Principle:** Featured Icons are dedicated components, not manually styled regular icons.

## 6. Context-Based Icon Selection

AI MUST select icons based on actual feature meaning and product requirements.

**Rules**
- Identify the function or action before selecting an icon.
- Use icons already mapped to the same function in GEMS Components.
- Choose semantically appropriate icons from the official GEMS library when needed.
- Maintain consistent icon usage across navigation, forms, tables, and related pages.
- Do not reuse sample icons for unrelated product features.
- Do not use icons solely for decorative purposes.
- Use clear text labels when icon meaning is ambiguous.
- Do not invent business features to justify icon usage.

## 7. Interaction States & Accessibility

Use official GEMS icon variants and parent component states.

**Supported States**
- Default
- Hover
- Focused
- Active / Selected
- Disabled
- Error / Success / Warning / Information, when applicable

**Rules**
- Follow original icon styling for each component state.
- Use official GEMS semantic colors and focus indicators.
- Maintain accessible names for icon-only actions.
- Use appropriate tooltips or labels when necessary.
- Do not rely on color alone to communicate important information.
- Keep decorative icons from creating redundant information.
- Do not invent custom hover, active, or disabled icon states.

## 8. Human Approval & Missing Icons

If no suitable official GEMS icon is available:

1. Check relevant GEMS icon categories and component references.
2. Identify suitable existing GEMS alternatives.
3. Ask the user to approve an existing alternative or provide a custom icon asset.
4. Use the selected icon only after explicit approval.

**Rules**
- Do not automatically use external icon libraries.
- Do not generate, redraw, or modify icons without authorization.
- Do not substitute icons with unrelated meanings.
- Do not interpret silence as approval.
- If an icon is optional, omit it rather than introducing an unapproved substitute.

## 9. Strict Icon Rules

**MUST**
- Use existing GEMS Figma Icon Components.
- Prioritize official component icons.
- Use Line/Outline Icons as the default.
- Follow official icon size, alignment, spacing, and placement.
- Use Featured Icon components when required.
- Maintain consistent semantic icon mapping.
- Follow GEMS component variants and interaction states.
- Reference relevant Page Samples and UX Patterns for contextual usage.
- Preserve accessibility and visual consistency.

**MUST NOT**
- Create new icons when official GEMS icons exist.
- Use external icon libraries or emoji substitutes.
- Invent icon sizes, styles, variants, or states.
- Modify original icon stroke, fill, proportions, or dimensions.
- Replace official component icons based on visual preference.
- Mix Line and Filled Icons arbitrarily.
- Create Featured Icons manually using regular icons and custom backgrounds.
- Add unnecessary icons for decoration.
- Substitute missing icons without human approval.
- Detach existing icon components unnecessarily.

**Fallback:** If an appropriate GEMS icon is unavailable, request Human Approval for an existing alternative or custom asset. If the icon is optional, use a text-only component.

**Core Principle:** Component icons take priority. Line/Outline is the default style. Icon sizes and Featured Icons MUST follow official GEMS specifications. Use icons only when they communicate function or meaning.
