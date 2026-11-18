
# GEMS Design System — Foundation / Typography

> **MANDATORY:** All UI text MUST use official GEMS Figma Text Styles. Applies to all pages, dashboards, forms, tables, components, and UX patterns.

## 1. Sources & Priority

**Source of Truth**
- [GEMS Typography](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=12-1127)
- GEMS Components, Page Samples & UX Pattern Samples within the same Figma Design System.

**Priority Order**
1. **Official Text Styles:** Apply existing GEMS Figma Text Styles directly, preserving all typography properties.
2. **GEMS Components:** Follow Text Styles defined for each component, variant, size, and breakpoint.
3. **Page Samples & UX Patterns:** Read relevant examples directly from GEMS Figma to determine actual typography usage and hierarchy.
4. **General UI/UX Principles:** Apply only when GEMS has no specific guidance.

Read only references relevant to the current task. Do not scan unrelated pages or components.

Official GEMS Text Styles and component specifications always take priority.

## 2. Available Text Styles

**Font Family:** Inter

| Text Style | Font Size | Line Height |
|---|---|---|
| `display 2xl` | 72px | 90px |
| `display xl` | 60px | 72px |
| `display lg` | 48px | 60px |
| `display md` | 36px | 44px |
| `display sm` | 30px | 38px |
| `display xs` | 24px | 32px |
| `text xl` | 20px | 30px |
| `text lg` | 18px | 28px |
| `text md` | 16px | 24px |
| `text sm` | 14px | 20px |
| `text xs` | 12px | 18px |

**Available Font Weights**

| Weight | Value |
|---|---|
| `regular` | 400 |
| `medium` | 500 |
| `semibold` | 600 |
| `bold` | 700 |

- Use only existing Text Style combinations from GEMS Figma.
- Apply complete Text Styles, preserving original font family, size, weight, line height, and letter spacing.
- Do not configure typography properties manually when an official style exists.

## 3. Typography Usage & Hierarchy

Select Text Styles based on official GEMS component specifications, relevant Page Samples, UX Patterns, and content hierarchy.

**GEMS Page Header Example**

| UI Element | Text Style |
|---|---|
| Page Header Title | `display xs / semibold` |
| Page Header Description | `text md / regular` |
| Page Header Navigation | `text sm / medium` |
| Page Header Action Label | `text sm / semibold` |
| Page Header Search Text | `text md / regular` |

Reference: [GEMS Page Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-7175)

**Application Rules**
- Read relevant GEMS Components, Page Samples, and UX Patterns to determine typography usage.
- Follow original Text Styles assigned to reusable components.
- Maintain consistent typography for elements with similar purposes.
- Use general visual hierarchy only when no specific GEMS guidance exists.
- For undefined usage, select an existing `display *` or `text *` style according to content hierarchy and readability.
- Preserve official Text Styles across desktop and mobile unless GEMS specifies different breakpoint styles.
- Adjust container, spacing, or text wrapping without modifying Text Style properties.
- Text color MUST follow GEMS Foundation Color Guidelines.
- Do not copy manual typography values from samples that conflict with official Text Styles.
- Do not use product-specific CCM typography as the General standard.

## 4. Strict Typography Rules

**MUST**
- Use existing GEMS Figma Text Styles.
- Preserve original Text Style references and properties.
- Follow official component typography specifications.
- Read relevant Page Samples and UX Patterns for contextual usage.
- Maintain consistent typography hierarchy across related UI screens.

**MUST NOT**
- Create new or duplicate Text Styles.
- Hardcode typography values outside existing GEMS Text Styles.
- Invent font sizes, weights, line heights, or letter spacing.
- Modify or override official Text Style properties.
- Detach existing Text Style references unnecessarily.
- Copy unsupported manual typography values from sample designs.
- Introduce external font families or typography scales.

**Fallback:** If no specific component or sample guidance exists, select the most appropriate existing GEMS Text Style based on content purpose and visual hierarchy. Never create a new Text Style.

**Core Principle:** Use existing GEMS Text Styles, not manually configured typography. Follow official component specifications before general UI/UX preferences.
