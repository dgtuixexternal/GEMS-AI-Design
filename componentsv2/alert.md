
# GEMS Design System — Components / Alert

> **MANDATORY:** All Alerts MUST use existing GEMS General Alert components and their official Figma variants. AI MUST determine whether an Alert is needed based on the actual product context, HSD/BRD, and GEMS usage patterns. CCM components and custom Alert designs are strictly prohibited.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Alert — Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=23-1651)
- [GEMS Alert — Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=612-8756)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **GEMS Alert:** Official component structure, properties, variants, and responsive styling.
2. **GEMS Foundation:** Official colors, typography, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, hierarchy, and placement.
4. **HSD/BRD & System Data:** Business conditions, message content, validation, permissions, and workflow behavior.
5. **General UI/UX Principles:** Fallback only when no GEMS-specific guidance exists.

For visual decisions, GEMS is the source of truth. For business behavior and factual content, follow HSD/BRD and actual system data.

---

## 2. Purpose & Component Selection

Alert communicates important information, warnings, errors, validation results, or confirmed outcomes that users need to understand within the current page or workflow.

**Use Alert when:**
- Important information must remain visible in context.
- Users need to understand a warning, requirement, or process impact.
- Validation results affect the next step.
- A process error requires explanation or recovery.
- A confirmed outcome requires persistent information.

**Do not automatically add Alert to every page.**

### Alert vs Other Components

| User Need | Correct Component |
|---|---|
| Important contextual information | **Alert** |
| Persistent warning or process impact | **Alert** |
| Validation summary across fields or records | **Alert + Field/Row Validation** |
| Brief success/error feedback | **Toast / Notification** |
| Confirmation before proceeding | **Modal** |
| Error on one input field | **Input Validation** |
| Status inside a data table | **Badge** |
| No records or content available | **Empty State** |
| Entire page fails to load | **GEMS Error State / Page Pattern** |
| Execute a primary action | **Button** |

AI MUST choose the component based on user needs and actual conditions, not merely because an Alert variant exists.

---

## 3. Available Variants & Properties

Use the original GEMS Alert instance and preserve its component reference.

| Property | Available Values |
|---|---|
| `Color` | `Default`, `Brand`, `Gray`, `Error`, `Warning`, `Success` |
| `Size` | `Floating`, `Full-width` |
| `Breakpoint` | `Desktop`, `Mobile` |

GEMS provides 24 official combinations across these properties.

**Component Rules**
- Use only existing GEMS General Alert variants.
- Preserve official layout, dimensions, padding, radius, icons, and typography.
- Select the correct variant rather than manually restyling another.
- Do not detach instances, duplicate the component, or reconstruct it from shapes.
- Do not create unsupported properties or combinations.
- **Never use CCM Alert components, variants, or styles.**

---

## 4. Semantic Colors

| Color | Meaning | Usage |
|---|---|---|
| `Default` | General information | Standard contextual notices |
| `Brand` | Emphasized information | Important product notices |
| `Gray` | Neutral information | General guidance and requirements |
| `Error` | Failure | Failed loading, validation, or processing |
| `Warning` | Risk or attention required | Incomplete requirements, partial validation problems |
| `Success` | Confirmed success | Completed result requiring persistent explanation |

**Rules**
- Color MUST reflect the actual meaning of the message.
- `Error` requires a genuine failure.
- `Warning` requires a real risk, incomplete requirement, or condition needing attention.
- `Success` requires a confirmed successful outcome.
- Use `Default` or `Gray` for neutral notices.
- Use `Brand` only when information warrants emphasis.
- Never use semantic colors solely for visual decoration.
- All color applications MUST follow `Foundation/color.md`.
- Primitive Brand-CCM and hardcoded HEX/RGB/HSL are prohibited.

---

## 5. Size & Breakpoint Usage

### Floating

Use `Size=Floating` for information associated with a specific content area.

**Recommended:**
- Card or section information.
- Form validation summaries.
- Detail-page notices.
- Contextual messages within content containers.

### Full-width

Use `Size=Full-width` for information affecting a wider content region or primary workflow.

**Recommended:**
- Page-level notices.
- Important information before main content.
- Validation summaries before data tables.
- Warnings affecting a complete workflow.

**Rules**
- Size MUST follow content scope and official GEMS usage.
- Do not use Full-width automatically for every Alert.
- Use official `Desktop` or `Mobile` breakpoint variants.
- Preserve responsive composition and text readability.
- Do not create Mobile layouts by manually shrinking Desktop instances.
- Do not invent custom dimensions or breakpoints.

---

## 6. Content Structure & Messaging

Follow the content structure supported by the selected GEMS variant.

| Element | Purpose | Usage |
|---|---|---|
| Container | Main Alert structure | Required |
| Icon | Reinforce semantic meaning | Follow official variant |
| Title | Explain primary condition | Clear and specific |
| Description | Explain details, impact, or next step | When relevant |
| Close | Dismiss the Alert | Only when supported and permitted |
| Action | Provide a next step | Only when supported and required |

Do not add unsupported elements solely to make the Alert appear more complete.

### Message Formula

For conditions requiring explanation:

**Condition → Impact → Next Action**

| Element | Example |
|---|---|
| Condition | 20 data tidak valid |
| Impact | Data tersebut tidak dapat diimpor |
| Next Action | Periksa keterangan pada tabel |

**Writing Rules**
- Use concise, clear, product-appropriate language.
- Titles MUST describe the actual condition.
- Descriptions SHOULD explain impact and next action when relevant.
- Follow official business terminology from HSD/BRD.
- Do not blame users or expose unnecessary technical details.
- Do not invent causes, record counts, statuses, results, or instructions.
- Avoid vague titles such as "Perhatian" when a specific condition can be stated.

---

## 7. Usage Scenarios

| Scenario | Color | Content Focus | Placement |
|---|---|---|---|
| General guidance | Default / Gray | Requirements or explanation | Near related content |
| Important product notice | Brand | Relevant announcement | Appropriate page section |
| Incomplete requirements | Warning | Missing information and next step | Near form or section |
| Partial validation failure | Warning | Valid/invalid results and process impact | Before validation table |
| Failed process | Error | Failure and recovery step | Near affected workflow |
| Failed data loading | Error | Loading problem and retry guidance | Relevant content region |
| Confirmed validation success | Success | Result and next step | Near validation result |
| Confirmed process success | Success | Outcome requiring explanation | Near affected content |

These mappings guide component selection; they do not authorize AI to invent business conditions.

### 7.1 Validation Result

Use for validation across multiple fields or records, including imports, uploads, and submissions.

**Requirements**
- Display actual valid and invalid results.
- Explain whether invalid records are skipped or block the entire process.
- Explain the next step when available.
- Preserve row-level and field-level error details.
- Position before the related validation table when consistent with GEMS patterns.

**Example**

**Title:** Hasil Validasi Data Impor

**Description:** 180 data valid siap diimpor. Sebanyak 20 data tidak valid tidak akan diimpor. Periksa keterangan pada tabel.

**Recommended configuration:** `Warning / Full-width / Desktop`, placed before the validation table.

*Example data is illustrative. Generated designs MUST use actual system results.*

**Critical:** Never assume partial import is allowed or that valid records are automatically ready for import. Follow the actual business policy.

### 7.2 Incomplete Information

Use when required information is missing.

- Explain what users must complete.
- Help users locate affected fields or sections.
- Keep individual field validation visible.
- Do not bypass required-data restrictions.

**Example:** "Lengkapi dokumen wajib sebelum mengirim pengajuan."

### 7.3 Warning

Use for conditions requiring attention without necessarily indicating total failure.

- Explain the risk or consequence.
- Provide an actionable next step if available.
- Do not use Warning simply to attract attention.

**Example:** "Sebagian data tidak memenuhi persyaratan. Periksa detail sebelum melanjutkan."

### 7.4 Error

Use for failed operations affecting the user's task.

- Identify the operation that failed.
- Explain recovery steps when available.
- Keep the message relevant while the issue persists.
- Use the official Error State pattern if the entire page cannot display its content.

**Example:** "Data gagal dimuat. Silakan coba kembali."

### 7.5 Success

Use only after system confirmation when the success message needs to remain visible.

- State the confirmed outcome.
- Explain relevant next steps.
- Prefer Toast for brief feedback.

**Example:** "Validasi berhasil. Seluruh data memenuhi persyaratan."

### 7.6 Informational

Use for general requirements, operational notes, or process explanations.

- Prefer `Default` or `Gray`.
- Use `Brand` only for justified emphasis.
- Do not turn neutral information into Error or Warning.

---

## 8. Placement & Layout

Place each Alert close to the content or workflow it describes.

| Placement | Context | Guidance |
|---|---|---|
| Page-Level | Entire page or primary workflow | Near Page Header or before main content |
| Section-Level | One content group | Inside or above relevant section |
| Form-Level | Form completion or submission | Near form; preserve field validation |
| Table-Level | Multi-record validation or processing | Before table; preserve row details |
| Mobile | Contextual information on narrow screens | Use official Mobile variant |

**Rules**
- Follow GEMS Page Samples and UX Patterns for actual placement.
- Avoid repeating the same message across multiple sections.
- Do not separate Alert from the affected content.
- Do not obscure important controls.
- Prefer one accurate Alert over multiple redundant Alerts.
- Do not introduce unsupported nesting or component compositions.

---

## 9. States, Actions & Behavior

### State Behavior

| Condition | Expected Behavior |
|---|---|
| Relevant condition becomes active | Display Alert |
| System information changes | Update Alert content |
| Issue is resolved | Update or remove Alert according to requirements |
| Process fails | Display accurate failure information |
| Process succeeds | Display confirmed outcome if persistent notice is needed |
| User dismisses Alert | Hide message only when dismissal is allowed |

### Dismissible Alert

- Close control MUST follow official GEMS styling and behavior.
- Dismissal only hides the message; it does not resolve the underlying issue.
- Do not assume every Alert is dismissible.
- Critical information must remain accessible when dismissal is permitted.
- Follow HSD/BRD for visibility, persistence, and dismissal rules.

### Alert with Action

If supported by the official component and business requirements, Alert may guide users to a relevant action.

**Example actions:**
- Coba Lagi
- Periksa Data
- Lihat Detail

**Rules**
- Action labels MUST describe actual available behavior.
- Action controls MUST follow official GEMS Button guidelines.
- Actions MUST respect permissions and workflow restrictions.
- Do not add actions solely for visual completeness.
- Do not perform destructive operations through Alert without required confirmation.
- Do not introduce unsupported buttons or interactions.

---

## 10. Foundation & Component Dependencies

All Alert elements MUST use existing GEMS Foundation styles.

### Foundation References

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Semantic colors, backgrounds, text, borders, and contrast |
| `Foundation/typography.md` | Official Text Styles for titles, descriptions, and labels |
| `Foundation/spacing-dan-radius.md` | Official padding, gaps, spacing, and corner radius |
| `Foundation/effect-styles.md` | Effects only when present in the official variant |
| `Foundation/icons.md` | Official semantic icons, sizes, and styling |
| `Foundation/misc-icons.md` | Specialized icons only when explicitly supported |
| `Foundation/design-annotations.md` | Official component usage specifications |

### Related Components

- **Button:** Alert actions MUST use GEMS Button.
- **Input / Dropdown:** Alert summaries MUST NOT replace field-level validation.
- **Badge:** Table status MUST use Badge when appropriate.
- **Tooltip:** Use for short supplementary explanations, not persistent warnings.
- **Progress Indicator:** Shows progress; Alert explains relevant issues or outcomes.

**Visual Rules**
- Preserve original GEMS component and style references.
- Apply complete official Text Styles.
- Use GEMS General semantic colors.
- Follow official spacing, radius, and icon sizes.
- Do not add decorative shadows unless defined by GEMS.
- Do not use CCM styling under any circumstances.

---

## 11. Accessibility Requirements

- Communicate meaning through text, not color or icon alone.
- Preserve readable contrast through GEMS color tokens.
- Maintain logical Title and Description reading order.
- Ensure Close and Action controls support keyboard interaction and visible focus.
- Provide accessible names for icon-only Close controls.
- Use appropriate announcement semantics: `role="alert"` for urgent information and `role="status"` for nonurgent updates when applicable.
- Do not make every informational Alert an urgent announcement.
- Do not make the container keyboard-focusable without a meaningful interaction.
- Preserve accessibility across Desktop and Mobile variants.

---

## 12. Strict AI Rules

### MUST

1. Use the original **GEMS General Alert** component.
2. Preserve supported `Color`, `Size`, and `Breakpoint` variants.
3. Determine whether Alert is genuinely needed.
4. Choose semantic colors based on actual conditions.
5. Select Size and placement based on content scope and GEMS patterns.
6. Use official GEMS Foundation styles and related component guidelines.
7. Derive message content and behavior from HSD/BRD and actual system data.
8. Explain condition, impact, and next action when relevant.
9. Follow GEMS Page Samples and UX Patterns for contextual usage.
10. Preserve accessibility and responsive behavior.
11. Request Human Approval before introducing unsupported patterns or behaviors.

### MUST NOT

1. **Use CCM components, CCM variants, or CCM styles.**
2. Create custom, duplicate, or detached Alert components.
3. Invent colors, sizes, breakpoints, icons, or interactions.
4. Hardcode styling values outside official GEMS styles.
5. Add Alert automatically to every page or process.
6. Replace Toast, Modal, Badge, Input Validation, or Empty State without valid reasons.
7. Invent business conditions, validation results, counts, or workflow behavior.
8. Assume success before system confirmation.
9. Assume all Alerts can be dismissed or contain actions.
10. Treat dismissal as resolving a business issue.
11. Use Alert to execute unconfirmed destructive actions.
12. Introduce unsupported designs or behaviors without Human Approval.

---

## 13. AI Usage Decision

When designing a screen, follow this decision order:

1. **Identify Condition:** Read HSD/BRD and available system data.
2. **Determine Necessity:** Decide whether users need persistent contextual information. If not, do not add Alert.
3. **Choose Component:** Confirm Alert is more appropriate than Toast, Modal, Badge, Input Validation, or Empty State.
4. **Select Variant:** Choose official GEMS `Color`, `Size`, and `Breakpoint`.
5. **Define Content:** Write accurate Title and Description, including impact and next action where relevant.
6. **Determine Placement:** Follow the appropriate GEMS Page Sample or UX Pattern.
7. **Apply Styling:** Preserve official GEMS component references and Foundation styles.
8. **Define Behavior:** Use Close and Action only when supported by GEMS and product requirements.

**Fallback:** If the needed variation, action, or business behavior is not defined in GEMS or HSD/BRD, request Human Approval before introducing it. Do not independently create a replacement component.

> **FINAL INSTRUCTION:** Use official **GEMS General Alert** components only when the UI genuinely requires an Alert. Semantic meaning determines Color, content scope determines Size, and target layout determines Breakpoint. Message content and behavior MUST reflect actual product requirements. **CCM is strictly prohibited.**
