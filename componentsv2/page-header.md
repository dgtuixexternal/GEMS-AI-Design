
# GEMS Design System — Components / Page Header

> **MANDATORY:** All Page Headers MUST use existing GEMS General Page Header components and supported Figma variants. AI MUST determine the appropriate header style, content, and whether action buttons are necessary based on page purpose, user tasks, HSD/BRD, and relevant GEMS Page Samples & UX Patterns. CCM components and unsupported designs are strictly prohibited.

> **CORE PRINCIPLE:** A Page Header communicates page identity, context, and relevant actions. A Page Header does not need a Button to be complete. Every Button must serve a real user task.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Page Header — Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-7175)
- [GEMS Page Header — General Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-7905)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **GEMS General Page Header:** Official structure, variants, layout, and responsive specifications.
2. **GEMS Foundation:** Typography, color, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, action placement, hierarchy, and composition.
4. **HSD/BRD:** Page purpose, content, user permissions, and business workflows.
5. **General UI/UX Principles:** Fallback only when no GEMS-specific guidance exists.

GEMS defines visual implementation. Product requirements determine content, actions, and behavior.

Read only the relevant references needed for the current page.

---

## 2. Purpose & When to Use

Page Header establishes the identity and context of the current page.

**Primary Purposes**
- Identify the current page.
- Explain its purpose when needed.
- Establish information hierarchy.
- Display relevant contextual information.
- Provide authorized page-level actions when necessary.
- Support appropriate navigation or entity information.

### When to Use

Page Header is commonly used for:
- Dashboard.
- Data List / Data Table.
- Detail Page.
- Form Page.
- Reports / Analytics.
- Settings / Configuration.
- Entity or Profile Page.

Follow the relevant GEMS Page Sample to determine the correct composition.

### When NOT to Use

Do not automatically add a standard Page Header to:
- Authentication screens with dedicated layouts.
- Modal or Dialog content.
- Tooltips or Dropdowns.
- Individual page sections.
- Components with their own dedicated header.
- Full-screen experiences using another approved GEMS pattern.

**Page Header is a page-level component, not a universal heading component.**

---

## 3. Available Variants & Properties

### Official Properties

| Property | Available Values |
|---|---|
| `Style` | `Simple`, `Simple-with-badge`, `Avatar`, `Banner avatar`, `Banner avatar centered`, `Banner simple`, `Banner simple centered` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Official Variant Availability

| Style | Desktop | Mobile |
|---|---|---|
| `Simple` | Available | Available |
| `Simple-with-badge` | Available | Not available |
| `Avatar` | Available | Available |
| `Banner avatar` | Available | Available |
| `Banner avatar centered` | Available | Available |
| `Banner simple` | Available | Available |
| `Banner simple centered` | Available | Available |

Use only supported combinations in the official GEMS General component.

**Component Rules**
- MUST use existing GEMS General Page Header instances.
- MUST preserve original Figma component references.
- MUST preserve official structure, typography, spacing, dimensions, and alignment.
- MUST NOT create unsupported variants or breakpoints.
- MUST NOT detach or manually reconstruct official Page Header components.
- MUST NOT invent a Mobile `Simple-with-badge` variant.

---

## 4. Strict CCM Restriction

The GEMS Figma file contains:
- `Page header CCM`
- `Style=Complex` within CCM
- CCM-specific Simple Page Headers
- `Main Button CCM`

**All CCM components, variants, buttons, and styling are prohibited.**

**Rules**
- NEVER use `Page header CCM`.
- NEVER use CCM `Style=Complex`.
- NEVER use `Main Button CCM`.
- NEVER use CCM-specific layout or styling as a General reference.
- Do not select components based solely on visual similarity.
- Complex page requirements MUST be handled using supported GEMS General components and Page Patterns.

**A complex page does not justify using a CCM Page Header.**

---

## 5. Page Header Style Selection

Select Style based on page purpose and content requirements.

| Style | Recommended Context | Usage Rule |
|---|---|---|
| `Simple` | Dashboard, List, Form, Report, Settings | Standard page identity and relevant actions |
| `Simple-with-badge` | Pages requiring contextual Badge | Use only when Badge adds meaningful information |
| `Avatar` | Profile or person-related detail | Requires relevant identity data |
| `Banner simple` | Pages requiring expanded contextual header | Follow approved GEMS Banner usage |
| `Banner simple centered` | Centered contextual presentation | Use only when supported by page pattern |
| `Banner avatar` | Identity-focused Banner | Requires meaningful entity identity |
| `Banner avatar centered` | Centered identity-focused Banner | Follow official GEMS composition |

### Selection Rules

- Prefer the simplest suitable General variant.
- Use Banner only when the page context supports it.
- Use Avatar only when meaningful person/entity information exists.
- Use Badge only when relevant contextual information is available.
- Do not introduce visual elements merely to make the header more attractive.
- Do not automatically choose Banner for Dashboard or Detail Pages.
- Preserve the original GEMS composition.

---

## 6. Page Header Content Structure

Page Header may contain the following supported elements depending on the selected variant.

| Element | Purpose | Usage |
|---|---|---|
| Page Title | Identify current page | Primary |
| Description | Explain page purpose | When useful |
| Navigation | Provide navigation context | When supported |
| Action Buttons | Perform relevant page-level actions | Only when necessary |
| Search | Locate relevant content | When supported and required |
| Badge | Display contextual status/information | When meaningful |
| Avatar | Identify person/entity | Identity-focused variants |
| Banner | Extended contextual presentation | Banner variants |

**Rules**
- Not every Page Header requires every element.
- Preserve the selected component's official structure.
- Do not add unsupported elements for visual completeness.
- Do not copy unrelated content from GEMS examples.
- Use actual product information and terminology.
- Avoid redundancy between Page Header and page content.

---

## 7. Typography & Content Hierarchy

All Page Header typography MUST follow official GEMS Figma Text Styles.

### GEMS Page Header Typography Reference

| UI Element | Text Style |
|---|---|
| Page Header Title | `display xs / semibold` |
| Page Header Description | `text md / regular` |
| Page Header Navigation | `text sm / medium` |
| Page Header Action Label | `text sm / semibold` |
| Page Header Search Text | `text md / regular` |

These are contextual references. The original component's current Figma Text Styles remain the source of truth.

### Title

- MUST identify the current page accurately.
- SHOULD use concise business terminology.
- MUST remain consistent with corresponding navigation labels.
- MUST NOT use vague or misleading titles.
- MUST NOT invent page purposes.

**Examples**
- Kelola Transportasi
- Daftar Karyawan
- Detail Pengajuan
- Laporan Operasional
- Pengaturan

### Description

- Explain the page purpose when additional context helps.
- Avoid repeating the Title without adding information.
- Keep wording concise and actionable when appropriate.
- Follow HSD/BRD terminology.
- Do not invent features or workflow behavior.

**Example**

Title: `Kelola Transportasi`

Description: `Kelola penempatan penumpang dan jadwal transportasi.`

Examples are illustrative. Generated content MUST reflect actual product requirements.

### Typography Rules

- Apply official GEMS Text Styles directly.
- Preserve font family, size, weight, line height, and letter spacing.
- Do not modify typography manually to fit layouts.
- Adjust spacing and text wrapping through supported GEMS patterns.
- Follow `Foundation/typography.md`.

---

## 8. Page Header Action Button Decision

> **MANDATORY:** AI MUST determine whether a Page Header requires action buttons before adding them. Buttons MUST NOT be included automatically.

### 8.1 When a Button Is Needed

Use a Page Header Button only when:
- A relevant page-level action exists.
- The action helps users accomplish a primary task.
- HSD/BRD defines the action.
- The current user role has permission.
- GEMS Page Samples or UX Patterns support its placement.

### 8.2 Action Decision Matrix

| Page Type | Button Requirement | Possible Action |
|---|---|---|
| Dashboard | Optional | Relevant business action |
| Data List | Based on requirements | Tambah Data |
| Detail Page | Based on permissions | Edit |
| Form Page | Follow Form UX Pattern | Simpan / Kirim |
| Report | Based on available features | Export Data |
| Settings | Based on interaction | Simpan Perubahan |
| Read-only Page | Usually unnecessary | No action unless required |

These are examples, not mandatory actions.

### 8.3 When NOT to Add a Button

Do not add a Page Header Button when:
- No meaningful page-level action exists.
- The page is primarily informational or read-only.
- The action is unavailable to the user's role.
- The action already exists in a more appropriate location.
- Adding the action would duplicate existing controls without purpose.
- The button has no real workflow or destination.

**A Page Header without action buttons is a valid and complete GEMS design.**

### 8.4 Action Priority

When actions are required:

1. Identify the page's primary user task.
2. Determine the most relevant action.
3. Include secondary actions only when necessary.
4. Choose official GEMS Button variants.
5. Follow the selected Page Header and UX Pattern for placement.

**Rules**
- Prioritize actual user tasks over visual completeness.
- Do not invent Create, Edit, Delete, Export, Refresh, or Submit actions.
- Do not add unnecessary secondary buttons.
- Do not assume every List Page needs `Tambah Data`.
- Do not assume every Report needs `Export`.
- Do not assume every Detail Page needs `Edit`.

### 8.5 Action Placement

- Follow the official GEMS Page Header structure.
- Use relevant Page Samples for primary and secondary action positioning.
- Avoid duplicating actions already placed in Table Toolbar, Form Footer, or other approved locations.
- For Mobile, follow the official responsive composition.
- Do not force Desktop action placement onto Mobile.
- Do not manually create unsupported button arrangements.

### 8.6 Button Component Rules

- MUST use official GEMS General Button components.
- MUST follow `components/button.md`.
- MUST preserve button size, variant, icon, state, and typography.
- MUST NOT use `Main Button CCM`.
- MUST NOT create custom buttons.
- MUST NOT introduce unsupported actions.

### 8.7 Destructive Actions

- Do not automatically place Delete or other destructive actions as primary Page Header actions.
- Respect workflow permissions and record states.
- Use official GEMS confirmation patterns when required.
- Follow GEMS Modal and Background Overlay guidelines.

---

## 9. Navigation & Search

### Navigation

Use Page Header navigation only when supported by the selected variant and product structure.

**Rules**
- Use actual page hierarchy and available routes.
- Keep terminology consistent with Application Navigation.
- Do not invent destinations or breadcrumbs.
- Avoid duplicating navigation elements unnecessarily.
- Follow official GEMS patterns.

### Search

Use Search only when:
- Relevant searchable content exists.
- HSD/BRD supports searching.
- The selected GEMS Page Header pattern supports Search.

**Rules**
- Use official GEMS Search/Input components.
- Searchable fields MUST exist in the data.
- Do not add Search merely to fill empty space.
- Do not duplicate Table Search without a valid purpose.
- Follow official responsive behavior.

---

## 10. Badge, Avatar & Banner Usage

### Badge

- Use only when meaningful contextual information exists.
- Use official GEMS Badge components.
- Follow `components/badge.md`.
- Do not invent status labels or semantic meanings.
- Do not use Badge as an action control.

### Avatar

- Use only for relevant person or entity identity.
- Use official GEMS Avatar components.
- Preserve real identity information or approved fallback behavior.
- Do not generate unrelated identities.
- Do not use Avatar for decoration.

### Banner

- Use only official GEMS Banner Page Header variants.
- Preserve original background, layout, and alignment.
- Do not introduce unsupported images, gradients, or effects.
- Do not automatically convert Simple Page Headers into Banners.
- Follow the relevant GEMS Page Sample.

---

## 11. Page-Level Usage

### 11.1 Dashboard

**Recommended**
- Simple Page Header.
- Clear Title.
- Optional Description.
- Actions only when relevant.

**Rules**
- Do not overload Page Header with KPI metrics.
- Place Charts and KPI Cards in the main content area.
- Do not add Buttons merely because the page is a Dashboard.
- Follow relevant GEMS Dashboard Page Samples.

### 11.2 Data List / Data Table

**Recommended**
- Simple Page Header.
- Accurate page identity.
- Optional primary action when supported.

**Rules**
- Use Add/Create only when authorized.
- Place search, filters, and table controls according to GEMS patterns.
- Avoid duplicating toolbar actions.
- Follow `components/data-table.md`.

### 11.3 Detail Page

**Recommended**
- Simple, Avatar, or appropriate official variant.

**Rules**
- Display accurate record identity.
- Use Badge for relevant statuses.
- Show Edit or other actions only when permitted.
- Do not invent entity information or actions.

### 11.4 Form Page

**Recommended**
- Simple Page Header or the official GEMS Form Page pattern.

**Rules**
- Clearly identify the form's purpose.
- Determine action placement from the relevant UX Pattern.
- Save, Submit, Cancel, or Back do not automatically belong in Page Header.
- Avoid duplicating Form Footer actions.
- Follow actual workflow requirements.

### 11.5 Report / Analytics

**Recommended**
- Simple Page Header.
- Appropriate reporting context.
- Export only when supported.

**Rules**
- Do not place analytics charts inside Page Header unless officially supported.
- Keep filters in appropriate GEMS locations.
- Do not invent export formats or reporting actions.

### 11.6 Settings / Configuration

**Recommended**
- Simple Page Header.

**Rules**
- Display only relevant configuration context.
- Show Save action only when the settings workflow requires it.
- Do not add unnecessary action buttons to read-only settings.

---

## 12. Responsive Behavior

### Desktop

- Use official `Breakpoint=Desktop` variants.
- Preserve layout, typography, spacing, and alignment.
- Maintain clear hierarchy between Title, Description, and actions.
- Avoid overcrowding the header.

### Mobile

- Use official `Breakpoint=Mobile` variants.
- Maintain Title and Description readability.
- Follow official action positioning and wrapping.
- Preserve essential page context.
- Do not manually shrink Desktop components.
- Do not create unsupported Mobile variants.

### Responsive Rules

- Use only existing Style/Breakpoint combinations.
- Do not remove essential actions without an approved alternative.
- Do not force Desktop button arrangements onto Mobile.
- Follow GEMS Page Samples for responsive behavior.
- Request Human Approval when required responsive behavior is unsupported.

---

## 13. Foundation & Component Dependencies

All Page Headers MUST follow GEMS Foundation.

### Foundation References

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | General colors, text, backgrounds, borders |
| `Foundation/typography.md` | Official Page Header Text Styles |
| `Foundation/spacing-dan-radius.md` | Layout spacing, padding, gaps, radius |
| `Foundation/effect-styles.md` | Official effects |
| `Foundation/icons.md` | Navigation and action icons |
| `Foundation/misc-icons.md` | Specialized icons where relevant |
| `Foundation/logo.md` | Product logo usage when applicable |
| `Foundation/application-navigation` | Navigation hierarchy |
| `Foundation/design-annotations.md` | Component specifications and annotations |

### Related Components

| Requirement | Related Guideline |
|---|---|
| Action Buttons | `components/button.md` |
| Grouped Actions | `components/button-group.md` |
| Contextual Status | `components/badge.md` |
| Identity | GEMS Avatar |
| Search | `components/input.md` |
| Data List | `components/data-table.md` |
| Confirmation | GEMS Modal + `components/bg-overlay.md` |
| Action Feedback | `components/notification.md` |

Use actual repository paths where filenames differ.

### Visual Rules

- Preserve original GEMS General component references.
- Apply existing GEMS Text Styles directly.
- Use official GEMS General color tokens.
- Preserve spacing, radius, effects, and icon sizes.
- Do not manually recreate Page Header layouts.
- Do not add decorative backgrounds or shadows unless defined by GEMS.
- Do not hardcode HEX/RGB/HSL, typography, or unsupported dimensions.
- Do not use CCM components or CCM-derived styling.

---

## 14. Accessibility

**MUST**
- Provide a clear primary page heading.
- Maintain logical heading hierarchy.
- Preserve readable typography and contrast.
- Use understandable action labels.
- Ensure Buttons and navigation controls support keyboard access.
- Preserve visible focus states.
- Provide accessible names for icon-only actions.
- Maintain usability on Desktop and Mobile.

**MUST NOT**
- Hide essential page identity.
- Use decorative content instead of meaningful headings.
- Make noninteractive content appear clickable.
- Add inaccessible custom controls.
- Remove necessary context for visual minimalism.

---

## 15. Strict AI Rules

### MUST

1. Use existing **GEMS General Page Header** components.
2. Select the appropriate Style based on page purpose.
3. Preserve supported Style and Breakpoint combinations.
4. Determine whether action buttons are genuinely needed.
5. Include only relevant and authorized actions.
6. Use accurate Title, Description, and entity information.
7. Follow official GEMS typography and component layout.
8. Follow relevant GEMS Page Samples and UX Patterns.
9. Apply GEMS Foundation and related component guidelines.
10. Preserve responsive behavior and accessibility.
11. Request Human Approval for unsupported variants or interactions.

### MUST NOT

1. **Use Page header CCM, Main Button CCM, or CCM Style=Complex.**
2. Create custom, detached, or duplicate Page Header components.
3. Invent unsupported styles or breakpoints.
4. Automatically add Buttons to every Page Header.
5. Invent Create, Edit, Delete, Export, Refresh, or Submit functionality.
6. Add unnecessary Badges, Avatars, Banners, or Search controls.
7. Duplicate actions without a valid purpose.
8. Use Banner styles solely for decoration.
9. Invent page content or navigation destinations.
10. Replace official Page Header with manually assembled elements.
11. Force Desktop compositions onto Mobile.
12. Hardcode styling outside official GEMS.
13. Introduce unsupported designs without Human Approval.

---

## 16. AI Page Header Selection Decision

When designing a page:

1. **Identify Purpose:** Read HSD/BRD and determine the page's primary user task.
2. **Determine Header Need:** Identify whether the page requires a standard Page Header or a dedicated GEMS layout.
3. **Select Style:** Choose the simplest suitable official General variant.
4. **Select Breakpoint:** Use the appropriate supported Desktop or Mobile combination.
5. **Define Content:** Use accurate Title, Description, navigation, and entity information.
6. **Evaluate Actions:** Determine whether Buttons are necessary.
7. **Select Buttons:** Include only authorized actions that support real user tasks.
8. **Determine Placement:** Follow the relevant GEMS Page Sample or UX Pattern.
9. **Apply Foundation:** Preserve official typography, colors, spacing, radius, effects, and icons.
10. **Preserve Behavior:** Follow actual navigation, permissions, and responsive requirements.

### Human Approval

Request Human Approval when:
- No suitable GEMS General Page Header variant exists.
- An unsupported responsive composition is required.
- A new header interaction is proposed.
- Important business actions are undefined.
- A custom Page Header would otherwise be necessary.

Combine related questions into one confirmation to minimize Claude AI context usage.

### Fallback

If the requested Page Header composition is unsupported:
1. Prefer the closest suitable GEMS General variant.
2. Place additional functionality in appropriate official page components.
3. Request Human Approval before introducing unsupported designs.
4. Never substitute CCM components.

> **FINAL INSTRUCTION:** Use the simplest suitable **GEMS General Page Header** that clearly communicates page identity and context. AI MUST independently determine whether action buttons are necessary, include only authorized and meaningful actions, follow official GEMS Foundation and Page Samples, and strictly prohibit CCM.
