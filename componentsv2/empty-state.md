
# GEMS Design System — Components / Empty State

> **MANDATORY:** All empty-data interfaces MUST use official GEMS Empty State components and supported variants. AI MUST determine when Empty State is necessary, select the appropriate visual, and configure its content and actions according to product context, HSD/BRD, and official GEMS UX Patterns. CCM components and styling are strictly prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Empty State](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=398-1166)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1105-7310)

**Priority Order**
1. **Official Empty State:** Source of truth for structure, available variants, visual properties, and sizes.
2. **GEMS Foundation:** Colors, typography, icons, spacing, radius, and effects.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, layout, hierarchy, and placement.
4. **HSD/BRD:** Product content, permissions, workflow, and available actions.
5. **General UI/UX Principles:** Fallback when no specific GEMS pattern exists.

Official GEMS components have visual priority. Functional requirements MUST follow approved HSD/BRD.

**Strict Exclusion:** Never use CCM Empty State components, CCM illustrations, or CCM-specific styling.

---

## 2. Available Components & Variants

AI MUST reuse official GEMS component instances and supported properties.

### 2.1 Empty State

**Component:** `Empty state`

| Property | Available Values |
|---|---|
| `Icon` | `Featured icon`, `Illustration`, `File type icon` |
| `Size` | `sm`, `md`, `lg` |

### Visual Selection

| Variant | Recommended Usage |
|---|---|
| `Featured icon` | General empty states requiring a simple contextual icon |
| `Illustration` | More prominent empty states when the GEMS pattern supports illustration |
| `File type icon` | Empty states specifically related to files or documents |

**Rules**
- Select the visual according to content meaning and official GEMS examples.
- Preserve the original component anatomy.
- Use only supported sizes and properties.
- Do not replace official visuals with custom SVGs, emoji, or external illustrations.
- Do not automatically use the largest visual.
- Do not use decorative illustrations merely to fill unused space.

### 2.2 Illustration

**Component:** `Illustration`

**Available Properties**

| Property | Available Values |
|---|---|
| `Style` | `Cloud`, `Credit card`, `Documents`, `Box` |
| `Color` | `Primary`, `Gray` |
| `Size` | `sm`, `md`, `lg` |

**Illustration Selection**

| Style | Contextual Guidance |
|---|---|
| `Cloud` | Cloud-related content or services |
| `Credit card` | Payment or financial-card-related content |
| `Documents` | Documents, reports, records, or related information |
| `Box` | Items, packages, inventory, or related content |

These mappings are contextual recommendations. The official GEMS implementation and relevant Page Samples take priority.

**Color Rules**
- `Primary`: Use the official GEMS General primary visual.
- `Gray`: Use the official neutral illustration.
- Select color based on GEMS references and visual hierarchy.
- Do not create additional illustration colors.
- Never substitute Brand CCM for `Primary`.

---

## 3. When to Use Empty State

**Core Principle:**

> Empty State communicates that a specific content area currently has no data or matching results. It must explain the situation clearly and provide an appropriate next action only when useful.

### Usage Matrix

| Context | Empty State Usage |
|---|---|
| Dashboard | No relevant dashboard data is available |
| Data Table | No records exist or no records match the applied filters |
| Detail Page | A specific information section contains no data |
| Form | An optional collection or repeatable section has no entries |
| Attachments | No supporting files have been uploaded |
| Activity History | No activity has been recorded |
| Notifications | No notifications are available |
| Reports | No reports have been generated |
| Search | No results match the search criteria |
| Monitoring | No records meet the selected monitoring conditions |

AI MUST determine whether the empty condition applies to the entire page or only one content section.

### When NOT to Use

Do not use Empty State for:
- Initial loading or ongoing data fetching.
- Temporary processing.
- Network or server failures.
- Successful operations that already contain data.
- Normal informational descriptions.
- Decorative page fillers.
- Missing permissions when a dedicated access-restriction pattern is required.

Use the appropriate GEMS Loading Indicator, Alert, Notification, or other relevant feedback component instead.

---

## 4. Empty State Types & Content Rules

The following are functional situations, not additional Figma variants.

### 4.1 Initial Empty State

Use when no records have been created.

**Example**

- Title: `Belum Ada Data`
- Description: `Data yang ditambahkan akan ditampilkan di sini.`
- Action: `Tambah Data`, only when the user has permission and the action is supported.

**Rules**
- Explain what is missing.
- Provide a creation action only when appropriate.
- Follow the relevant product terminology.
- Do not force users to create data if the page is intentionally read-only.

### 4.2 Filtered Empty State

Use when records exist in the system but none match the selected filters.

**Example**

- Title: `Data Tidak Ditemukan`
- Description: `Tidak ada data yang sesuai dengan filter yang dipilih.`
- Action: `Reset Filter`, when supported.

**Rules**
- Preserve the user's filter context.
- Explain that the result is empty because of the applied criteria.
- Provide a way to adjust or reset filters where appropriate.
- Do not suggest creating a new record as the default solution.

### 4.3 Search Empty State

Use when a search returns no matching results.

**Example**

- Title: `Hasil Pencarian Tidak Ditemukan`
- Description: `Coba gunakan kata kunci lain.`
- Action: Optional, depending on the search interaction.

**Rules**
- Distinguish search results from a completely empty dataset.
- Preserve the search query until the user changes it.
- Provide relevant guidance.
- Do not display misleading messages claiming the system has no data.

### 4.4 Section Empty State

Use when a specific section has no content.

**Example**

- Title: `Belum Ada Dokumen`
- Description: `Dokumen pendukung akan ditampilkan di sini setelah ditambahkan.`

**Rules**
- Render Empty State inside the affected content container.
- Preserve surrounding page content.
- Use a size appropriate to the section.
- Do not replace the entire page when only one section is empty.

### 4.5 Read-Only Empty State

Use when no data is available and the user cannot create or modify it.

**Rules**
- Provide a clear explanation.
- Do not display unauthorized create actions.
- Do not imply the user can resolve the empty condition when no action is available.

---

## 5. Empty State Anatomy & Actions

AI MUST follow the anatomy and component properties available in the official GEMS instance.

### Content Anatomy

| Element | Purpose |
|---|---|
| Visual | Reinforces the empty condition |
| Title | Describes what is missing |
| Description | Explains the situation or what happens next |
| Action | Provides a relevant recovery or creation path when necessary |

Display optional elements only when supported by the GEMS component and appropriate to the workflow.

### Title Rules
- Keep titles concise and specific.
- Use product terminology.
- Describe the actual empty condition.
- Prefer meaningful titles over generic system messages.

### Description Rules
- Explain why the area is empty when known.
- Explain what the user can expect or do next.
- Avoid blaming users.
- Keep wording clear and actionable.
- Do not invent reasons for missing data.

### Action Rules

An Empty State **does not always require a button**.

| Situation | Recommended Action |
|---|---|
| No records created | Create action, if authorized |
| No search results | Adjust search or no action |
| No filtered results | Reset or adjust filters |
| No attachments | Upload action, if authorized |
| No activity history | Usually no action |
| No notifications | Usually no action |
| Read-only content | Usually no action |

**Action Requirements**
- Use only official GEMS Buttons.
- Display actions supported by HSD/BRD.
- Follow user permissions.
- Use the correct button hierarchy and variant.
- Do not introduce unnecessary primary actions.
- Never create a button that has no functional destination.

---

## 6. Empty State in CRUD & UX Patterns

### Create
- Display an initial Empty State when the relevant collection contains no records.
- Show the create action only if the role is permitted.
- Replace or update the Empty State after successful data creation.

### Read
- Show Empty State for genuinely empty sections or datasets.
- Distinguish missing data from inaccessible data.
- Preserve the page layout and section hierarchy.

### Update
- Use Empty State when an editable collection has no existing entries.
- Display add or edit-related actions only if supported.
- Do not display an empty condition while data is still loading.

### Delete
- When deletion results in an empty dataset, display the appropriate Empty State.
- Use the official GEMS confirmation pattern before deletion when required.
- Do not show Empty State before a deletion request has successfully completed.

### Approval / Rejection / Revision
- Use Empty State when a task queue or activity list contains no matching items.
- Keep labels aligned with the current workflow.
- Do not introduce approval actions when no eligible item exists.

---

## 7. Layout, Size & Placement

### Available Sizes

| Size | Recommended Context |
|---|---|
| `sm` | Compact sections and constrained containers |
| `md` | Standard content areas |
| `lg` | Prominent empty content regions where supported |

These are usage recommendations. The selected GEMS component and relevant Page Samples determine the actual sizing.

### Placement Rules

AI MUST:
- Position Empty State inside the affected content area.
- Follow official alignment and spacing.
- Preserve the component's icon, text, and action hierarchy.
- Use consistent placement across equivalent pages.
- Select a size based on the available container and GEMS references.
- Follow the official Desktop and Mobile layout behavior where defined.

AI MUST NOT:
- Stretch illustrations manually.
- Invent custom spacing or dimensions.
- Add unnecessary surrounding Card components.
- Add shadows or decorative backgrounds without GEMS reference.
- Place the Empty State outside its relevant content area.
- Change its alignment merely for aesthetic preference.

---

## 8. Relationship with Other GEMS Components

Empty State MUST follow all relevant existing GEMS guidelines.

### Foundation Dependencies

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official Brand General and neutral colors |
| `Foundation/typography.md` | Title and description Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, layout, and radius |
| `Foundation/effect-styles.md` | Official effects where applicable |
| `Foundation/icons.md` | General icon usage |
| `Foundation/misc-icons.md` | Featured Icon and File Type Icon |
| `Foundation/design-annotations.md` | Official design specifications and behavior |

### Related Components

- **Button:** Optional create, upload, reset, or recovery actions.
- **Data Table:** Empty datasets and filtered results.
- **Tabs:** Empty content inside the active tab.
- **Page Header / Section Header:** Page and section hierarchy.
- **Input / Dropdown:** Search and filter interactions.
- **File Upload:** Missing attachments.
- **Loading Indicator:** Loading before the empty condition is established.
- **Alert / Notification:** Errors and feedback requiring a different presentation.
- **Application Navigation:** Preserve surrounding page navigation.

Related components MUST retain their own GEMS specifications.

---

## 9. Empty, Loading & Error Distinction

AI MUST distinguish these conditions correctly.

| Condition | Appropriate Pattern |
|---|---|
| No data exists | GEMS Empty State |
| No search matches | GEMS Empty State with search-specific content |
| No filtered results | GEMS Empty State with filter-specific content |
| Data still loading | GEMS Loading Indicator |
| Request failed | GEMS error feedback pattern |
| User lacks access | Approved access-restriction pattern |
| Data successfully loaded | Display the actual content |

**Rules**
- Never show Empty State before determining that the result is genuinely empty.
- Never treat an API failure as an empty dataset.
- Never display fabricated data to avoid showing Empty State.
- When data becomes available, render the appropriate content component.
- Maintain consistency between the displayed condition, message, and available action.

---

## 10. Strict GEMS Compliance

**MUST**
- Use official GEMS Empty State components.
- Preserve existing component instances and properties.
- Select only supported icon and size variants.
- Use official GEMS Illustration variants when applicable.
- Match visual, title, description, and actions to the product context.
- Use existing GEMS Foundation styles.
- Follow relevant Page Samples and UX Patterns.
- Respect user roles and business permissions.
- Distinguish empty, loading, and error conditions.
- Keep Empty State behavior consistent across equivalent screens.

**MUST NOT**
- Use CCM components, illustrations, colors, or styling.
- Recreate GEMS Empty State using custom Frames.
- Invent unsupported illustrations, icons, sizes, or variants.
- Use external illustrations when the official component is available.
- Hardcode unsupported HEX/RGB/HSL, typography, spacing, radius, or effects.
- Use decorative visuals unrelated to the content.
- Add unnecessary buttons or actions.
- Show unauthorized actions.
- Treat API failures as empty results.
- Use generic content when a meaningful product-specific message is available.
- Modify official component structure without approval.

---

## 11. AI Selection & Human Approval

AI MUST determine:

1. **Condition:** Is the content genuinely empty?
2. **Scope:** Is the empty condition page-level or section-level?
3. **Context:** Is it initial, filtered, searched, or read-only?
4. **Component:** Which official GEMS Empty State variant is appropriate?
5. **Visual:** Should it use Featured Icon, Illustration, or File Type Icon?
6. **Size:** Which supported size matches the layout?
7. **Content:** What title and description fit the product?
8. **Action:** Does the user need a button, and is the action permitted?

Use HSD/BRD and official GEMS examples to resolve these decisions.

**Human Approval Required**

If a requirement needs a visual pattern, illustration, interaction, or component variant unavailable in GEMS, AI MUST request Human Approval before introducing a custom solution.

Combine unresolved questions into one concise confirmation. Do not repeatedly ask about information already available in product documentation.

**Fallback:** Use the closest suitable official GEMS Empty State component. Never invent unsupported visual properties or variants.

---

## 12. Final AI Instruction

**AI MUST use the official GEMS Empty State whenever a page or section requires empty-data feedback.**

Select the appropriate component, visual variant, size, content, and optional action based on actual data conditions, product requirements, and relevant GEMS Page Samples and UX Patterns.

An Empty State must communicate a meaningful condition. **Not every Empty State requires an illustration or an action button.**

Preserve official GEMS components, typography, colors, icons, spacing, radius, effects, and responsive behavior.

Never use CCM components, invent unsupported variants, or replace loading and error states with misleading Empty States.

**GEMS Design System is the single source of truth for Empty State visual specifications.**
