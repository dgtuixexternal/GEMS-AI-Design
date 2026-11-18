
# GEMS Design System — Foundation / Effect Styles

> **MANDATORY:** All UI effects MUST use official GEMS Figma Effect Styles. Apply effects only when required by component specifications, interaction states, or visual hierarchy.

## 1. Sources & Priority

**Source of Truth**
- [GEMS Effect Styles](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-7082)
- GEMS Components, Page Samples & UX Pattern Samples within the same Figma Design System.

**Priority Order**
1. **Official Effect Styles:** Use existing GEMS Figma Effect Styles directly.
2. **GEMS Components:** Follow effect specifications for each component, variant, and state.
3. **Page Samples & UX Patterns:** Read relevant examples directly from GEMS Figma to determine actual effect usage and visual hierarchy.
4. **General UI/UX Principles:** Apply only when GEMS has no specific guidance.

Read only references relevant to the current task. Do not scan unrelated pages or components.

Official GEMS Effect Styles and component specifications always take priority.

## 2. Available Effect Styles

**Shadows**
- `shadow-xs`
- `shadow-xs-skeuemorphic`
- `shadow-sm`
- `shadow-md`
- `shadow-lg`
- `shadow-xl`
- `shadow-2xl`
- `shadow-3xl`

**Focus Rings**
- `focus-ring`
- `focus-ring-error`
- `focus-ring-shadow-xs`
- `focus-ring-shadow-sm`
- `focus-ring-shadow-xs-skeuemorphic`
- `focus-ring-error-shadow-xs`
- `focus-ring-error-shadow-xs-skeuemorphic`

**Color Shadows**
- `red`

**Archive**
- `shadow 1`
- `shadow 2`
- `shadow 3`
- `shadow 4`

Apply existing Effect Styles directly from Figma. Preserve original effect properties and references. Archive styles are not the default for new UI.

## 3. Effect Usage & States

- Read relevant GEMS Components, Page Samples, and UX Patterns to understand where effects are applied.
- Follow original component effects, including variants and interaction states.
- Use shadows only when required for elevation, interaction, or visual separation.
- Apply official focus-ring and error effects when applicable.
- Preserve keyboard focus indicators for accessibility.
- Maintain consistent elevation across similar components.
- If an official component has no shadow, keep it without shadow.
- Do not add shadows solely to make UI appear more modern or decorative.
- Do not invent effects for states that have no specified effect.

**Supported States:** `Default` · `Hover` · `Focus` · `Active` · `Disabled` · `Error`

## 4. Strict Effect Rules

**MUST**
- Use existing GEMS Figma Effect Styles.
- Preserve original Effect Style references and properties.
- Follow official component effect specifications.
- Read relevant Page Samples and UX Patterns for contextual usage.
- Maintain consistent elevation and accessible focus indicators.

**MUST NOT**
- Create new or duplicate Effect Styles.
- Hardcode shadows, blur, spread, offset, or effect colors.
- Modify or override official Effect Style properties.
- Invent hover, focus, or error effects.
- Detach existing Effect Style references unnecessarily.
- Apply shadows automatically to every Card, Table, or Section.
- Add unnecessary decorative effects.
- Introduce external effect systems.
- Use Archive styles as the default for new components.

**Fallback:** If no effect is specified or functionally required, use no effect. When necessary, select an appropriate existing GEMS Effect Style without modifying its properties.

**Core Principle:** No unnecessary effects. Follow GEMS component specifications, not visual decoration preferences.
